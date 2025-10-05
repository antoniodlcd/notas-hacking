## Descripción
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:64573/) out.
## Solución
El reto se llama robot sans, entonces accedí al archivo robots.txt del proyecto y me salió esto:
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```
al convertir esa cadena de base64 me dieron la dirección de 2 archivos:
```
flag1.txt
js/myfile.txt
```
La llave estaba en "js/myfile.txt":
```
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}
```
## Notas
## Referencias
