## Descripción
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/50522/` ([link](https://jupiter.challenges.picoctf.org/problem/50522/)) or http://jupiter.challenges.picoctf.org:50522
## Solución
en los encabezados de la pagina sale eso:
```
user-agent

Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/140.0.0.0 Safari/537.36
```
usé este comando en la consola:
```
┌──(anton㉿anton)-[~/documentos]
└─$ curl https://jupiter.challenges.picoctf.org/problem/50522/flag -H "User-Agent:picobrowser" | grep picoCTF
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--      0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--    100  2115  100  2115    0     0   1962      0  0:00:01  0:00:01 --:--:--  1963
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{p1c0_s3cr3t_ag3nt_51414fa7}</code></p>
```
## Notas
## Referencias