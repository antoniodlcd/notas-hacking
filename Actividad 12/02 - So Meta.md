## Descripción
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/00efdf2961da1e21470ffc0d496c3cc2/pico_img.png).
## Solución
```
┌──(kali㉿kali)-[~/Documents/forensic/someta]
└─$ ls
pico_img.png
                                    
┌──(kali㉿kali)-[~/Documents/forensic/someta]
└─$ exiftool pico_img.png 
...
...
Artist                          : picoCTF{s0_m3ta_fec06741}

```

```
┌──(kali㉿kali)-[~/Documents/forensic/someta]
└─$ strings pico_img.png | grep picoCTF
picoCTF{s0_m3ta_fec06741}

```
## Notas
exiftool - es una herramienta que te ayuda a ver los metadatos de una imagen4
## Referencias
