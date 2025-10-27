## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg)
## Solución
Usé el comando zsteg para extraer la información oculta de la imagen, la herramienta me indicó que había 379140 bytes de datos extra después del final de la imagen, por lo que usé el siguiente comando para crear una copia del archivo a partir del byte exacto en el que empiezan los datos extra:
``` bash
dd if=dolls.jpg of=base_images.zip bs=1 skip=272492
```
Esto creó un zip que descomprimí y en él había otro archivo jpg.
Usé el mismo comando que con la primera imagen y seguían habiendo datos extra. En total fueron 4 imágenes y cuando extraje la información oculta de la 4ta encontré la bandera:
```
picoCTF{96fac089316e094d41ea046900197662}
```
## Notas
## Referencias
