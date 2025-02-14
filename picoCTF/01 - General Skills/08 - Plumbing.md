## Descripción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.
Hints:
1. Remember the flag format is picoCTF{XXXX}
2. What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)

## Solución 

```
SrRiv-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 41120 > datos
^C
SrRiv-picoctf@webshell:~$ la
.bash_logout  .bashrc  .lesshst  .profile  .python_history  .wget-hsts  README.txt  datos  file  flag
SrRiv-picoctf@webshell:~$ ls
README.txt  datos  file  flag
SrRiv-picoctf@webshell:~$ cat datos | grep pico 
picoCTF{nEtCat_Mast3ry_3214be47}
SrRiv-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 > datos
^C
SrRiv-picoctf@webshell:~$ cat datos | grep pico
picoCTF{digital_plumb3r_ea8bfec7}
SrRiv-picoctf@webshell:~$
```

## Notas adicionales 
## Referencias