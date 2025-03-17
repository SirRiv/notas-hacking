## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too

Hints: 
1. Does that encoding look familiar?
2. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución 

Checamos el archivo de Python y buscamos la contraseña con CyberChef. Para obtener la contraseña que se espera en el archivo de Python. 

```
if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
Convertimos de de Hexadecimal a ASCII

0x33 = 3
0x39 = 9
0x63 = c
0x65 = e

Contraseña necesaria 39ce

SrRiv-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/SrRiv-picoctf/level2.py", line 27, in <module>
    level_2_pw_check()
  File "/home/SrRiv-picoctf/level2.py", line 17, in level_2_pw_check
    user_pw = input("Please enter correct password for flag: ")
KeyboardInterrupt

SrRiv-picoctf@webshell:~$ nano level2.py 
SrRiv-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
SrRiv-picoctf@webshell:~$ 

picoCTF{tr45h_51ng1ng_502ec42e}


```
## Notas adicionales 
## Referencias