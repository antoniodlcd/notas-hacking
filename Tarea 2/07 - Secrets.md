## Descripción
We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:61273/).
## Solución
El código fuente de la página tenía una línea que mostraba una carpeta llamada secret/
```
 src="[secret/assets/DX1KYM.jpg](view-source:http://saturn.picoctf.net:59646/secret/assets/DX1KYM.jpg)"
```
Al acceder a esa carpeta, mostró una carpeta llamada hidden/
```
<link rel="stylesheet" href="[hidden/file.css](view-source:http://saturn.picoctf.net:59646/secret/hidden/file.css)" />
```
Y esta tenía otra llamada superhidden/
```
<link href="[superhidden/login.css](view-source:http://saturn.picoctf.net:59646/secret/hidden/superhidden/login.css)" rel="stylesheet" />
```
Esta última tenía la llave:
```
picoCTF{succ3ss_@h3n1c@10n_790d2615}
```
## Notas
## Referencias
