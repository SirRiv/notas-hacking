## Descripción
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!

## Solución

```
SrRiv-picoctf@webshell:~$ ls
README.txt  datos  file  flag  ltdis.sh  static  strings  warm
SrRiv-picoctf@webshell:~$ chmod +x static 
SrRiv-picoctf@webshell:~$ ./static
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
SrRiv-picoctf@webshell:~$ bash ltdis.sh
Attempting disassembly of  ...
objdump: 'a.out': No such file
objdump: section '.text' mentioned in a -j option, but not found in any input file
Disassembly failed!
Usage: ltdis.sh <program-file>
Bye!
SrRiv-picoctf@webshell:~$ bash ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
SrRiv-picoctf@webshell:~$ ls
README.txt  file  ltdis.sh  static.ltdis.strings.txt  strings
datos       flag  static    static.ltdis.x86_64.txt   warm
SrRiv-picoctf@webshell:~$ nano ltdis.sh
SrRiv-picoctf@webshell:~$ cat static.ltdis.strings.txt | grep pico
   1020 picoCTF{d15a5m_t34s3r_f5aeda17}
SrRiv-picoctf@webshell:~$ 

```

## Notas adicionales

## Referencias


