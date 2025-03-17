## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)

Hints:
1. On the webshell, use `ls` to see if both files are in the directory you are in
2. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución 

```
SrRiv-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py
--2025-03-17 02:08:52--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                        100%[====================================================================================================>]   1.25K  --.-KB/s    in 0s      

2025-03-17 02:08:52 (57.9 MB/s) - 'code.py' saved [1278/1278]

SrRiv-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt
--2025-03-17 02:09:02--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                   100%[====================================================================================================>]      27  --.-KB/s    in 0s      

2025-03-17 02:09:02 (14.3 MB/s) - 'codebook.txt' saved [27/27]

SrRiv-picoctf@webshell:~$ ls
code.py  codebook.txt
SrRiv-picoctf@webshell:~$ python code.py 
picoCTF{c0d3b00k_455157_7d102d7a}
SrRiv-picoctf@webshell:~$


picoCTF{c0d3b00k_455157_7d102d7a}
```

## Notas adicionales 
## Referencias