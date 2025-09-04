## Descripción
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!

## Solución
### Solución 1
```
antoniodlcd-picoctf@webshell:~$ ls     
ltdis.sh  static
antoniodlcd-picoctf@webshell:~$ strings static | grep picoCTF
picoCTF{d15a5m_t34s3r_f5aeda17}
antoniodlcd-picoctf@webshell:~$ 
```
### Solución 2
```
antoniodlcd-picoctf@webshell:~$ bash ltdis.sh static 
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
antoniodlcd-picoctf@webshell:~$ ls  
ltdis.sh  static  static.ltdis.strings.txt  static.ltdis.x86_64.txt
antoniodlcd-picoctf@webshell:~$ cat static
static                    static.ltdis.strings.txt  static.ltdis.x86_64.txt
antoniodlcd-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_f5aeda17}
antoniodlcd-picoctf@webshell:~$ 
```
## Notas
bash - es la terminal/intérprete que ejecuta los comandos en Linux
## Referencias
