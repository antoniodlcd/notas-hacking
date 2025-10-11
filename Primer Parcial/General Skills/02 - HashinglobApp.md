## Descripción
If you want to hash with the best, beat this test!`nc saturn.picoctf.net 54766`
## Solución
El reto te pide codificar con md5 un grupo de palabras:
```
┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 54766
Please md5 hash the text between quotes, excluding the quotes: 'stun guns'
Answer: 
d1bc34c1bbadaea803f9ab0284e25adf
d1bc34c1bbadaea803f9ab0284e25adf
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'chains'
Answer: 
ebe412db83c4bb837ebc25f3395fca6e
ebe412db83c4bb837ebc25f3395fca6e
Incorrect. Try again?
Answer: 
99469f92ab96d54efce3d605a4bb4fbe
99469f92ab96d54efce3d605a4bb4fbe
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Atlantis'
Answer: 
a425a3c39e1eaba4a378b0a08d80db9b
a425a3c39e1eaba4a378b0a08d80db9b
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_674c1de2}

```
## Notas
## Referencias