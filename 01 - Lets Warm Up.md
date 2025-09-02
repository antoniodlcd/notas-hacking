#Reto

## Descripción
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?
## Solución
usé una página para convertir de hex a ascii

p

picoCTF{p}

```python
>>> int(0x70)
112
>>> chr(112)
'p'
>>> quit()
```
## Notas
* Hay que subir las resueltas con el formato de las banderas "picoCTF{flag}"
* CyberChef es un sitio web que permite codifica y decodificar en diferentes formatos
## Referencias
https://neapay.com/online-tools/hex-to-ascii-converter.html