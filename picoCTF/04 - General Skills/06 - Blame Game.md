## Descripción
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/156/challenge.zip)

Hints:
1. In collaborative projects, many users can make many changes. How can you see the changes within one file?
2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3. You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
## Solución 

~~~
SrRiv-picoctf@webshell:~$ ls
challenge.zip  drop-in
SrRiv-picoctf@webshell:~$ cd drop-in/
SrRiv-picoctf@webshell:~/drop-in$ ls
message.py
SrRiv-picoctf@webshell:~/drop-in$ git log message.py
SrRiv-picoctf@webshell:~/drop-in$ 
~~~
## Notas adicionales 
## Referencias
