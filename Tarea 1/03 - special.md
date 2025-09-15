## Descripción
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)
## Solución
tuve que ver 2 videos para resolverlo.
En el primero la persona lo resolvió de una manera que no entendí (no entendí el cómo llego a esa conclusión) ;
```
Special$ find .
Find .
sh: 1: Find: not found
Special$ Clear & find .
Clear & find .
sh: 1: Clear: not found
.
./blargh
./blargh/flag.txt
./.cache
./.cache/motd.legal-displayed
Special$ Find .
Find .
sh: 1: Find: not found
Special$ & find .
& find .
sh: 1: Syntax error: "&" unexpected
Special$ Clear & cat ./blargh/flag.txt
Clear & cat ./blargh/flag.txt
sh: 1: Clear: not found
picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}Special$ 
```

En el segundo, la persona intentó varias formas hasta que llegó a la conclusión de que debía acceder a los comandos desde las rutas relativas de estos
```
Special$ ../usr/bin/ls
../usr/bin/ls
sh: 1: ../usr/bin/ls: not found
Special$ ../../usr/bin/ls
../../usr/bin/ls
blargh
Special$ ../../usr/bin/ls ./blargh
../../usr/bin/ls ./blargh
flag.txt
Special$ ../../usr/bin/cat ./blargh/flag.txt
../../usr/bin/cat ./blargh/flag.txt
picoCTF{5p311ch3ck_15_7h3_w0r57_f906e25a}Special$ 
```
## Notas
los comando de linux están guardados en el directorio /usr/bin
## Referencias
https://www.youtube.com/watch?v=K9H6i73ydMM&ab_channel=MartinCarlisle
https://www.youtube.com/watch?v=ukeBAbfiz2k&ab_channel=2xdropout