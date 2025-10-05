## Descripción
Do you know how to use the web inspector?Start searching [here](http://titan.picoctf.net:56324/) to find the flag
## Solución
El sitio tenía un link a un archivo llamado about.html, este sitio tenía la línea:
``` html
 <section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMWY4MzI2MTV9">
```
Al pasarle esa cadena a la página cyberchef , me dio la llave:
picoCTF{web_succ3ssfully_d3c0ded_1f832615}
## Notas
## Referencias
