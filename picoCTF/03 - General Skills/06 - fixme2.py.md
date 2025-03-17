## Descripción
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)

Hints:
1. Are equality and assignment the same symbol?
2. To view the file in the webshell, do: `$ nano fixme2.py`
3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución 

Corregimos el archivo de python para poder obtener la bandera.

```
SrRiv-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/5/fixme2.py
--2025-03-17 02:24:12--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                      100%[====================================================================================================>]   1.00K  --.-KB/s    in 0s      

2025-03-17 02:24:12 (52.1 MB/s) - 'fixme2.py' saved [1029/1029]

SrRiv-picoctf@webshell:~$ nano fixme2.py 
SrRiv-picoctf@webshell:~$ pyhton fixme2.py 
-bash: pyhton: command not found
SrRiv-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
SrRiv-picoctf@webshell:~$ 


picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}


```
## Notas adicionales 
## Referencias