## Descripción
Someone's commits seems to be preventing the program from working. Who is it?
## Solución
```
┌──(anton㉿anton)-[~/Documents]
└─$ ls
challenge.zip  drop-in

┌──(anton㉿anton)-[~/Documents]
└─$ cd drop-in/

┌──(anton㉿anton)-[~/Documents/drop-in]
└─$ ls -al
total 16
drwxr-xr-x 3 anton anton 4096 Sep 10 11:02 .
drwxr-xr-x 3 anton anton 4096 Sep 10 11:01 ..
drwxr-xr-x 8 anton anton 4096 Mar 11  2024 .git
-rwxr--r-- 1 anton anton   23 Sep 10 11:02 message.py

┌──(anton㉿anton)-[~/Documents/drop-in]
└─$ cd .git/

┌──(anton㉿anton)-[~/Documents/drop-in/.git]
└─$ ls -al
total 52
drwxr-xr-x   8 anton anton 4096 Mar 11  2024 .
drwxr-xr-x   3 anton anton 4096 Sep 10 11:02 ..
drwxr-xr-x   2 anton anton 4096 Mar 11  2024 branches
-rw-r--r--   1 anton anton   24 Mar 11  2024 COMMIT_EDITMSG
-rw-r--r--   1 anton anton   92 Mar 11  2024 config
-rw-r--r--   1 anton anton   73 Mar 11  2024 description
-rw-r--r--   1 anton anton   23 Mar 11  2024 HEAD
drwxr-xr-x   2 anton anton 4096 Mar 11  2024 hooks
-rw-r--r--   1 anton anton  145 Mar 11  2024 index
drwxr-xr-x   2 anton anton 4096 Mar 11  2024 info
drwxr-xr-x   3 anton anton 4096 Mar 11  2024 logs
drwxr-xr-x 221 anton anton 4096 Mar 11  2024 objects
drwxr-xr-x   4 anton anton 4096 Mar 11  2024 refs

┌──(anton㉿anton)-[~/Documents/drop-in/.git]
└─$ grep -r picoCTF{
logs/HEAD:05f26d123cde97b714aaae28ba8f18db3f385af5 2466febd40004b9ca644ce924181d07e23dcfaeb picoCTF{@sk_th3_1nt3rn_cfca95b2} <ops@picoctf.com> 1710202026 +0000 commit: optimize file size of prod code
logs/refs/heads/master:05f26d123cde97b714aaae28ba8f18db3f385af5 2466febd40004b9ca644ce924181d07e23dcfaeb picoCTF{@sk_th3_1nt3rn_cfca95b2} <ops@picoctf.com> 1710202026 +0000    commit: optimize file size of prod code

```
## Notas
con el grep puedes buscar la llave muy fácilmente
## Referencias
