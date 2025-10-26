## Descripción
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/5/unknown.zip).
## Solución
Descomprimí el archivo y al revisar los metadatos de la imagen que contenía encontré un texto cifrado con base64.
Usé la terminal para descifrarlo:
``` bash
┌──(kali㉿kali)-[~]
└─$ echo 'cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==' | base64 -d
picoCTF{ME74D47A_HIDD3N_4dabddcb}
```
## Notas
## Referencias
