## Descripción
Unzip this archive and find the flag.
- [Download zip file](https://artifacts.picoctf.net/c/504/big-zip-files.zip)

Hints:
1. Can grep be instructed to look at every file in a directory and its subdirectories?
## Solución 

```
SrRiv-picoctf@webshell:~$ grep -R picoCTF{
.python_history:'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}
SrRiv-picoctf@webshell:~$ 

picoCTF{gr3p_15_m4g1c_ef8790dc}

```

## Notas adicionales 
## Referencias