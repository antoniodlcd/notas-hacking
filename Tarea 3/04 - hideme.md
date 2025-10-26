## Descripción
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/260/flag.png).
## Solución
Usé la herramienta zsteg para extraer la información oculta de la imagen, y me dio esta respuesta:
``` bash
┌──(kali㉿kali)-[~/Documents/forensic/hideme]
└─$ zsteg flag.png              
[?] 3266 bytes of extra data after image end (IEND), offset = 0x9b3b
extradata:0         .. file: Zip archive data, made by v3.0 UNIX, extract using at least v1.0, last modified Mar 16 2023 02:01:54, uncompressed size 0, method=store
```
que indica que después de que el archivo png terminara había otro archivo de tipo zip que empieza en el bit 0x9b3b del archivo original.

Convertí el offset que me dio a decimal:
``` bash
┌──(kali㉿kali)-[~/Documents/forensic/hideme]
└─$ echo $((0x9b3b))                                      
39739

```

Usé la herramienta dd (Disk Dump) para crear una copia del archivo a partir del bit 39739 y guardarla con el nombre bandera.zip:
``` bash
┌──(kali㉿kali)-[~/Documents/forensic/hideme]
└─$ dd if=flag.png of=bandera.zip bs=1 skip=39739
```
Al descomprimir el archivo resultante encontré una imagen llamada flag.png y al abrirla me mostró la bandera:
```
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_ad9f6587}
```
## Notas
zsteg - es una herramienta que ayuda a detectar datos ocultos en imágenes PNG y BMP
## Referencias
