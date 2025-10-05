## Descripción
Can you get the flag? Go to this [website](http://saturn.picoctf.net:60845/) and see what you can discover.
## Solución
Al ver el código fuente del sitio, encontré el link a la página de login:
``` html
<form role="form" action="[login.php](view-source:http://saturn.picoctf.net:65017/login.php)" method="post">
```
Esta pagina tenía el link a un js llamado secure.js:
``` html
<script src="[secure.js](view-source:http://saturn.picoctf.net:65017/secure.js)"></script>
```
Este archivo tenía el usuario y la contraseña del admin:
``` JavaScript
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
Los introduje en el login del sitio y me dio la llave:
```
picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
```
## Notas
## Referencias
