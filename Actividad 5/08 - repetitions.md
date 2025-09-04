## Descripción
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/475/enc_flag).
## Solución
```
antoniodlcd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/475/enc_flag
--2025-09-03 17:49:40--  https://artifacts.picoctf.net/c/475/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.72, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag             100%[=====================>]     349  --.-KB/s    in 0s      

2025-09-03 17:49:40 (110 MB/s) - 'enc_flag' saved [349/349]

antoniodlcd-picoctf@webshell:~$ ls
README.txt  enc_flag
antoniodlcd-picoctf@webshell:~$ cat enc_flag 
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKVVZXcE9VazFXV2toT1dHUllDbUY2UWpSWk1GWlhWa2RHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
antoniodlcd-picoctf@webshell:~$ cat enc_flag | base
base32    base64    basename  basenc    
antoniodlcd-picoctf@webshell:~$ cat enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
cGljb0NURntiYXNlNjRfbjNzdDNkX2RpYzBkIW44X2Qwd25sMDRkM2RfNDkyNzY3ZDJ9Cg==
antoniodlcd-picoctf@webshell:~$ cat enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_492767d2}
antoniodlcd-picoctf@webshell:~$ 
```
## Notas
base64 -d - decodifica un texto en base64
## Referencias
