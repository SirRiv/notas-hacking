## Descripción
We found this [file](https://mercury.picoctf.net/static/06a5e4ab22ba52cd66a038d51a6cc07b/tunn3l_v1s10n). Recover the flag.
Hints:
1. Weird that it won't display right...
## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ xxd -l 100 tunn3l_v1s10n
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........
00000020: 0000 5826 2c00 2516 0000 2516 0000 0000  ..X&,.%...%.....
00000030: 0000 0000 0000 231a 1727 1e1b 2920 1d2a  ......#..'..) .*
00000040: 211e 261d 1a31 2825 352c 2933 2a27 382f  !.&..1(%5,)3*'8/
00000050: 2c2f 2623 332a 262d 2420 3b32 2e32 2925  ,/&#3*&-$ ;2.2)%
00000060: 3027 2333                                0'#3
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ cp tunn3l_v1s10n flag.bmp
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ ls
flag.bmp  tunn3l_v1s10n
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ hexeditor flag.bmp
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ eog flag.bmp
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ exiftool flag.bmp
ExifTool Version Number         : 12.76
File Name                       : flag.bmp
Directory                       : .
File Size                       : 2.9 MB
File Modification Date/Time     : 2025:05:06 13:03:31-06:00
File Access Date/Time           : 2025:05:06 13:03:37-06:00
File Inode Change Date/Time     : 2025:05:06 13:03:31-06:00
File Permissions                : -rw-r--r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Image Size                      : 1134x306
Megapixels                      : 0.347
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ hexeditor flag.bmp
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ hexeditor flag.bmp
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$ eog flag.bmp
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/tunn3l$
~~~

~~~
picoCTF{qu1t3_a_v13w_2020}
~~~
## Notas adicionales 

Modificamos con hexeditor el bmp para arreglar el archivo, cambiamos los offset 0xA, 0xE y 0x16 para arreglar el archivo. 
## Referencias
