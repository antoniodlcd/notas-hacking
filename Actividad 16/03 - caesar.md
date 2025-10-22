## Descripción
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext).
## Solución
el archivo tenía el siguiente texto:
```
picoCTF{dspttjohuifsvcjdpoabrkttds} 
```
la encriptación caesar consiste en desplazar cierto número de veces las letras en el abecedario, usando cyberchef y rotándolo 25 veces conseguí la llave:
```
picoCTF{crossingtherubiconzaqjsscr}
```
## Notas
cyberchef:
Formula: ROT13
Amount: 25
## Referencias
