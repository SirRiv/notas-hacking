## Descripción

My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/178/challenge.zip)
Hints:
1. `git branch -a` will let you see available branches
2. How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
3. Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.

## Solución 

~~~
rRiv-picoctf@webshell:~$ ls
challenge.zip  drop-in
SrRiv-picoctf@webshell:~$ cd drop-in/
SrRiv-picoctf@webshell:~/drop-in$ ls
flag.py
SrRiv-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
SrRiv-picoctf@webshell:~/drop-in$ git log flag.py
SrRiv-picoctf@webshell:~/drop-in$ 
SrRiv-picoctf@webshell:~/drop-in$ 
SrRiv-picoctf@webshell:~/drop-in$ git branch -a
SrRiv-picoctf@webshell:~/drop-in$ git branch feature/part-1
fatal: A branch named 'feature/part-1' already exists.
SrRiv-picoctf@webshell:~/drop-in$ git checkout feature/part-1
Switched to branch 'feature/part-1'
SrRiv-picoctf@webshell:~/drop-in$ ls
flag.py
SrRiv-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')SrRiv-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
SrRiv-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')SrRiv-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
SrRiv-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_6c06cec1}")



picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_6c06cec1}
~~~
## Notas adicionales 
## Referencias
