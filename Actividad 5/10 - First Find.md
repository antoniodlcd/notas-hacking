## Descripción
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)
## Solución
```
antoniodlcd-picoctf@webshell:~$ ls files
13771.txt.utf-8  acceptable_books  satisfactory_books
14789.txt.utf-8  adequate_books
antoniodlcd-picoctf@webshell:~$ cd files/
antoniodlcd-picoctf@webshell:~/files$ ls
13771.txt.utf-8  acceptable_books  satisfactory_books
14789.txt.utf-8  adequate_books
antoniodlcd-picoctf@webshell:~/files$ find . -name "uber-secret.txt"
./adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
antoniodlcd-picoctf@webshell:~/files$ find . -name "uber-secret.txt" | cd
antoniodlcd-picoctf@webshell:~/files$ cd adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/ 
antoniodlcd-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secre
ts/deepest_secrets$ ls
uber-secret.txt
antoniodlcd-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secre
ts/deepest_secrets$ wc uber-secret.txt 
 1  1 31 uber-secret.txt
antoniodlcd-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secre
ts/deepest_secrets$ cat uber-secret.txt | grep picoCTF
picoCTF{f1nd_15_f457_ab443fd1}
antoniodlcd-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secre
ts/deepest_secrets$ 
```
## Notas
## Referencias
