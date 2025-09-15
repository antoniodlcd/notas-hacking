## Descripción
What was I last working on? I remember writing a note to help me remember...
## Solución
```
┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ cat message.txt
This is what I was working on, but I'd need to look at my commit history to know why...
┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ ls -al
total 16
drwxr-xr-x 3 anton anton 4096 Mar  9  2024 .
drwxr-xr-x 3 anton anton 4096 Sep 14 15:27 ..
drwxr-xr-x 8 anton anton 4096 Mar  9  2024 .git
-rw-r--r-- 1 anton anton   87 Mar  9  2024 message.txt

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ cd .git

┌──(anton㉿anton)-[~/documentos/drop-in/.git]
└─$ ls -al
total 52
drwxr-xr-x 8 anton anton 4096 Mar  9  2024 .
drwxr-xr-x 3 anton anton 4096 Mar  9  2024 ..
drwxr-xr-x 2 anton anton 4096 Mar  9  2024 branches
-rw-r--r-- 1 anton anton   30 Mar  9  2024 COMMIT_EDITMSG
-rw-r--r-- 1 anton anton   92 Mar  9  2024 config
-rw-r--r-- 1 anton anton   73 Mar  9  2024 description
-rw-r--r-- 1 anton anton   23 Mar  9  2024 HEAD
drwxr-xr-x 2 anton anton 4096 Mar  9  2024 hooks
-rw-r--r-- 1 anton anton  145 Mar  9  2024 index
drwxr-xr-x 2 anton anton 4096 Mar  9  2024 info
drwxr-xr-x 3 anton anton 4096 Mar  9  2024 logs
drwxr-xr-x 7 anton anton 4096 Mar  9  2024 objects
drwxr-xr-x 4 anton anton 4096 Mar  9  2024 refs

┌──(anton㉿anton)-[~/documentos/drop-in/.git]
└─$ git log --graph
* commit 3339c144a0c78dc2fbd3403d2fb37d3830be5d94 (HEAD -> master)
  Author: picoCTF <ops@picoctf.com>
  Date:   Sat Mar 9 21:10:22 2024 +0000

      picoCTF{t1m3m@ch1n3_d3161c0f}
```
## Notas
## Referencias
