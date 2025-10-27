## Descripción
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/c00c449c3b08daaccacca6f9d5c55d49/Forensics%20is%20fun.pptm)
## Solución
Navegando por los directorios encontré un archivo llamado hidden, ese archivo contenía una cadena que parecía estar cifrada, puse lo siguiente en la terminal de linux:
``` bash
┌──(kali㉿kali)-[~/…/forensic/macrohardweakedge/ppt/slideMasters]
└─$ echo 'Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q ' | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```
## Notas
## Referencias
