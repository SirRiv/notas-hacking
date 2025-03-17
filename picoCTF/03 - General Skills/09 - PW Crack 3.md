## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

Hints:
1. To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
2. To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
3. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 



```
SrRiv-picoctf@webshell:~$ bvi level3.hash.bin 

bvi version 1.4.0 Copyright (C) 1996-2014 by Gerhard Buergmann
SrRiv-picoctf@webshell:~$ nano level3.py 
SrRiv-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/SrRiv-picoctf/level3.py", line 39, in <module>
    level_3_pw_check()
  File "/home/SrRiv-picoctf/level3.py", line 27, in level_3_pw_check
    user_pw = input("Please enter correct password for flag: ")
KeyboardInterrupt

SrRiv-picoctf@webshell:~$ nano level3.py 
SrRiv-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
SrRiv-picoctf@webshell:~$ 
```
## Notas adicionales 
## Referencias