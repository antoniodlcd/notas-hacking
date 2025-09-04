## Descripción
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm) has extraordinarily helpful information...

## Solución
```
antoniodlcd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
--2025-09-03 16:51:36--  https://mercury.picoctf.net/static/fc1d77192c544314efece5dd309092e3/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                 100%[=====================>]  10.68K  --.-KB/s    in 0s      

2025-09-03 16:51:36 (242 MB/s) - 'warm' saved [10936/10936]

antoniodlcd-picoctf@webshell:~$ chmod +x warm 
antoniodlcd-picoctf@webshell:~$ ./ warm 
-bash: ./: Is a directory
antoniodlcd-picoctf@webshell:~$ ls
strings  warm
antoniodlcd-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
antoniodlcd-picoctf@webshell:~$ warm -h
-bash: warm: command not found
antoniodlcd-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_6635aa47}
antoniodlcd-picoctf@webshell:~$ 
```
## Notas
## Referencias
