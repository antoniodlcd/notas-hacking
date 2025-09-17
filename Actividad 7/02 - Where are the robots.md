## Descripción
Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/36474/` ([link](https://jupiter.challenges.picoctf.org/problem/36474/)) or http://jupiter.challenges.picoctf.org:36474
## Solución
al escribir /robots.txt al final de la liga me llevó a esta página:
```
https://jupiter.challenges.picoctf.org/problem/36474/robots.txt/
User-agent: *
Disallow: /477ce.html
```
al sustituir /robots.txt por el que nos proporcionó, mostró la bandera:
```
https://jupiter.challenges.picoctf.org/problem/36474/477ce.html
Guess you found the robots  
picoCTF{ca1cu1at1ng_Mach1n3s_477ce}
```
## Notas
## Referencias