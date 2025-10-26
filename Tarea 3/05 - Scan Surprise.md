## Descripción
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:
- [challenge.zip](https://artifacts.picoctf.net/c_atlas/16/challenge.zip)
The same files are accessible via SSH here:`ssh -p 53522 ctf-player@atlas.picoctf.net`Using the password `6abf4a82`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Solución
Al descomprimir el archivo encontré un archivo png que contiene un código qr.
Usé el comando zbarimg para convertir el codigo qr a texto:
```
┌──(kali㉿kali)-[~/…/scansurprice/home/ctf-player/drop-in]
└─$ ls
flag.png
                                                                                             
┌──(kali㉿kali)-[~/…/scansurprice/home/ctf-player/drop-in]
└─$ zbarimg flag.png 
QR-Code:picoCTF{p33k_@_b00_7843f77c}
scanned 1 barcode symbols from 1 images in 0.01 seconds


```
## Notas
## Referencias
