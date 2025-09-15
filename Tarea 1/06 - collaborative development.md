## Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?
## Solución
```
┌──(anton㉿anton)-[~/documentos]
└─$ cd drop-in/
┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
  ┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ git checkout feature/part-1
Switched to branch 'feature/part-1'

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ ls -al
total 16
drwxr-xr-x 3 anton anton 4096 Sep 14 14:49 .
drwxr-xr-x 3 anton anton 4096 Sep 14 14:47 ..
-rw-r--r-- 1 anton anton   64 Sep 14 14:49 flag.py
drwxr-xr-x 8 anton anton 4096 Sep 14 14:49 .git

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ python3 flag.py
Printing the flag...
picoCTF{t3@mw0rk_
┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ git checkout feature/part-2
Switched to branch 'feature/part-2'

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ python3 flag.py
Printing the flag...
m@k3s_th3_dr3@m_
┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ git checkout feature/part-3
Switched to branch 'feature/part-3'

┌──(anton㉿anton)-[~/documentos/drop-in]
└─$ python3 flag.py
Printing the flag...
w0rk_4c24302f}

```
## Notas
## Referencias
