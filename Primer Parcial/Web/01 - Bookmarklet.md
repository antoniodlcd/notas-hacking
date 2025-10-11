## Descripción
Why search for the flag when I can make a bookmarklet to print it for me?Browse [here](http://titan.picoctf.net:50919/), and find the flag!
## Solución
En la página se mostraba un código de javaScript que guardé en un bookmark:
```
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÔÅÐÙí";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
    
```
Al momento de acceder a este, me mostró la bandera desencriptada
```
picoCTF{p@g3_turn3r_1d1ba7e0}
```
## Notas
## Referencias
