## Descripción
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090
## Solución
Hice log in con el nombre de usuario anton y recuperé la cookie llamada "name" y con el valor:
```
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYW50b24ifQ.B45VupvUo-LZNvpphuMLxKF7zgOfSYLQm7nCQfLKHwI
```
usé el programa john en kali con el diccionario rockyou.txt
```
john token -w=/usr/share/wordlists/rockyou.txt
```
## Notas

## Referencias
https://github.com/openwall/john
https://jwt.lannysport.net/
