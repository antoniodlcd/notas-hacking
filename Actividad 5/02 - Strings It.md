## Descripción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?
## Solución
```
antoniodlcd-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_827aee91}
antoniodlcd-picoctf@webshell:~$ 
```
## Notas
strings -  Display printable strings in a file
grep no puede mostrar caracteres de ejecutables
chmod - Permite cambiar los permisos a un archivo
## Referencias
