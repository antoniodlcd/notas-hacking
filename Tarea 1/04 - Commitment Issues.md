## Descripción
I accidentally wrote the flag down. Good thing I deleted it!
## Solución
```
┌──(anton㉿anton)-[~/documentos/drop-in/.git]
└─$ ls -al
total 52
drwxr-xr-x  8 anton anton 4096 Sep 14 15:04 .
drwxr-xr-x  3 anton anton 4096 Sep 14 15:02 ..
drwxr-xr-x  2 anton anton 4096 Mar  9  2024 branches
-rw-r--r--  1 anton anton   22 Mar  9  2024 COMMIT_EDITMSG
-rw-r--r--  1 anton anton   92 Mar  9  2024 config
-rw-r--r--  1 anton anton   73 Mar  9  2024 description
-rw-r--r--  1 anton anton   23 Mar  9  2024 HEAD
drwxr-xr-x  2 anton anton 4096 Mar  9  2024 hooks
-rw-r--r--  1 anton anton  145 Mar  9  2024 index
drwxr-xr-x  2 anton anton 4096 Mar  9  2024 info
drwxr-xr-x  3 anton anton 4096 Mar  9  2024 logs
drwxr-xr-x 10 anton anton 4096 Mar  9  2024 objects
drwxr-xr-x  4 anton anton 4096 Mar  9  2024 refs

┌──(anton㉿anton)-[~/documentos/drop-in/.git]
└─$ git log --graph
* commit a6dca68e4310585eac3b5c9caf0f75967dfe972c (HEAD -> master)
| Author: picoCTF <ops@picoctf.com>
| Date:   Sat Mar 9 21:10:06 2024 +0000
|
|     remove sensitive info
|
* commit e720dc26a1a55405fbdf4d338d465335c439fb3e
  Author: picoCTF <ops@picoctf.com>
  Date:   Sat Mar 9 21:10:06 2024 +0000

      create flag
┌──(anton㉿anton)-[~/documentos/drop-in/.git]
└─$ git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e
fatal: this operation must be run in a work tree

┌──(anton㉿anton)-[~/documentos/drop-in/.git]
└─$ cd ..

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e
Note: switching to 'e720dc26a1a55405fbdf4d338d465335c439fb3e'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at e720dc2 create flag

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ ls -al
total 16
drwxr-xr-x 3 anton anton 4096 Sep 14 15:16 .
drwxr-xr-x 3 anton anton 4096 Sep 14 15:00 ..
drwxr-xr-x 8 anton anton 4096 Sep 14 15:16 .git
-rw-r--r-- 1 anton anton   27 Sep 14 15:16 message.txt

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ cat message.txt
picoCTF{s@n1t1z3_7246792d}
```

## Notas
git log --graph - muestra todos los commits que se han hecho y su informacion
git checkout <idCommit> - puedes acceder a los commits anteriores usando su id

## Referencias
