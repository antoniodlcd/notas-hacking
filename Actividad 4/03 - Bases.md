## Descripción
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.
## Solución
### Forma 1
CypherChef
Formula: From Base64
picoCTF{l3arn_th3_r0p35}

### Forma 2
``` python
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1').decode()
'l3arn_th3_r0p35'
>>> 
```
## Notas
## Referencias
https://webshell.picoctf.org/
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE