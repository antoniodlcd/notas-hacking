## Descripción
How well can you perfom basic binary operations?
## Solución
```
┌──(anton㉿anton)-[~/Documents]
└─$ nc titan.picoctf.net 63786

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10100101
Binary Number 2: 01011110


Question 1/6:
Operation 1: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11110010010110
Correct!

Question 2/6:
Operation 2: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111111
Correct!

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 00101111
Correct!

Question 4/6:
Operation 4: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 0100101
Incorrect. Try again
Enter the binary result: 01001010
Incorrect. Try again
Enter the binary result: 01001011
Incorrect. Try again
Enter the binary result: 01001010
Incorrect. Try again
Enter the binary result: 0101001010
Correct!

Question 5/6:
Operation 5: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100000011
Correct!

Question 6/6:
Operation 6: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 00000100
Correct!

Enter the results of the last operation in hexadecimal: 04

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_aeaf4b09}
```

## Notas
## Referencias
https://es.planetcalc.com/911/
https://gchq.github.io/CyberChef/#recipe=From_Binary('Space',8)To_Hex('Space',0)&input=MDAwMDAxMDA