## Descripción
Description
How well can you perfom basic binary operations?
Additional details will be available after launching your challenge instance.


## Solución 

Usamos CyberChef

~~~
SrRiv-picoctf@webshell:~$ nc titan.picoctf.net 57126

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01001001
Binary Number 2: 11110111


Question 1/6:
Operation 1: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 100011001101111
Correct!

Question 2/6:
Operation 2: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 01000001
Correct!

Question 3/6:
Operation 3: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01111011
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 101000000
Correct!

Question 5/6:
Operation 5: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 10010010
Correct!

Question 6/6:
Operation 6: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111111
Correct!

Enter the results of the last operation in hexadecimal: 0xFF

Correct answer!




The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_1367e2c6}
~~~
## Notas adicionales 
## Referencias
