
## Descripción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?

Hints: 
1. [strings](https://linux.die.net/man/1/strings)
## Solución 
Mediante el comando strings y el uso de grep
```
SrRiv-picoctf@webshell:~$ ls
README.txt  strings
SrRiv-picoctf@webshell:~$ file strings
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=94ec6b5e9cef175e834e0f7fcaedeaa167603c90, not stripped
SrRiv-picoctf@webshell:~$ ls -la strings
-rw-rw-r-- 1 SrRiv-picoctf SrRiv-picoctf 776032 Oct 26  2020 strings
SrRiv-picoctf@webshell:~$ chmod +x strings
SrRiv-picoctf@webshell:~$ ls -la strings
-rwxrwxr-x 1 SrRiv-picoctf SrRiv-picoctf 776032 Oct 26  2020 strings
SrRiv-picoctf@webshell:~$ strings strings | grep pico 
picoCTF{5tRIng5_1T_d66c7bb7}
SrRiv-picoctf@webshell:~$ 
```

## Notas adicionales 
## Referencias
