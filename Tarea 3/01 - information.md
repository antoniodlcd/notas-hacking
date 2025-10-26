## Descripción
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/c28a959c5605d5f67480d5dd3a77f302/cat.jpg)
## Solución
Usé el comando exiftool para ver los metadatos de la imagen y en licencia tenía el valor:
```
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
```
Copié y pegue el valor en ciberchef y me dio la llave:
```
picoCTF{the_m3tadata_1s_modified}
```
## Notas
ciberchef
receta: From Base64
## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnQwYUdWZmJUTjBZV1JoZEdGZk1YTmZiVzlrYVdacFpXUjk