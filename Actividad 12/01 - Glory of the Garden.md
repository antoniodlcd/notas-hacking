## Descripción
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

## Solución
```
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/forensic/gloryofthegarden]
└─$ ls    
garden.jpg
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/forensic/gloryofthegarden]
└─$ file garden.jpg 
garden.jpg: JPEG image data, JFIF standard 1.01, resolution (DPI), density 72x72, segment length 16, baseline, precision 8, 2999x2249, components 3
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/forensic/gloryofthegarden]
└─$ open garden.jpg 
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/forensic/gloryofthegarden]
└─$ cat garden.jpg | grep picoCTF
grep: (standard input): binary file matches
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/forensic/gloryofthegarden]
└─$ strings garden.jpg | grep picoCTF
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"

```

## Notas
xxd - es un comando que te permite visualizar los bytes de un archivo

## Referencias
