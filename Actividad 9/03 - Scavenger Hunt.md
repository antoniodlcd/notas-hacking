## Descripción
There is some interesting information hidden around this site [http://mercury.picoctf.net:39491/](http://mercury.picoctf.net:39491/). Can you find it?
## Solución
al inspeccionar el código fuente de la pagina, me di cuenta que ahí estaba la primer parte de la llave. El head tenía el link a dos archivos; un .css y un .js.

``` css
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */
```
``` JavaScript
/* How can I keep Google from indexing my website? */
```
accedí al archivo robots.txt
```
http://mercury.picoctf.net:39491/robots.txt

User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?
```
el profe dejo un link a una pagina sobre apache, que habla sobre un archivo .htaccess
```
http://mercury.picoctf.net:39491/.htaccess

# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```
el profe dejo un link a una pagina sobre un archivo llamad .DS_Store en mac
```
http://mercury.picoctf.net:39491/.DS_Store

Congrats! You completed the scavenger hunt. Part 5: _f7ce8828}
```
## Notas
## Referencias
https://httpd.apache.org/docs/2.4/en/howto/htaccess.html
https://en.wikipedia.org/wiki/.DS_Store 