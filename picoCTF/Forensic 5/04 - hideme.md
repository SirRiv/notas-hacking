## Descripción
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/261/flag.png).

## Solución 

```
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme$ eog flag.png
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme$ zsteg flag.png
[?] 3180 bytes of extra data after image end (IEND), offset = 0x9b3b
extradata:0         .. file: Zip archive data, at least v1.0 to extract, compression method=store
    00000000: 50 4b 03 04 0a 00 00 00  00 00 3c 10 70 56 00 00  |PK........<.pV..|
    00000010: 00 00 00 00 00 00 00 00  00 00 07 00 1c 00 73 65  |..............se|
    00000020: 63 72 65 74 2f 55 54 09  00 03 93 78 12 64 93 78  |cret/UT....x.d.x|
    00000030: 12 64 75 78 0b 00 01 04  00 00 00 00 04 00 00 00  |.dux............|
    00000040: 00 50 4b 03 04 14 00 00  00 08 00 3c 10 70 56 75  |.PK........<.pVu|
    00000050: 61 47 c7 2a 0b 00 00 c7  0b 00 00 0f 00 1c 00 73  |aG.*...........s|
    00000060: 65 63 72 65 74 2f 66 6c  61 67 2e 70 6e 67 55 54  |ecret/flag.pngUT|
    00000070: 09 00 03 93 78 12 64 93  78 12 64 75 78 0b 00 01  |....x.d.x.dux...|
    00000080: 04 00 00 00 00 04 00 00  00 00 cd 56 57 3c db 8f  |...........VW<..|
    00000090: 16 ff a9 52 ad 51 45 ed  22 66 8b 98 0d 4a ed 68  |...R.QE."f...J.h|
    000000a0: ec 99 9a 6d cc 34 66 43  cc 88 59 a3 43 69 5d 1f  |...m.4fC..Y.Ci].|
    000000b0: 54 cd 52 5b aa 8a 18 b1  7a cd 96 52 b5 47 a3 f6  |T.R[....z..R.G..|
    000000c0: 9e a1 34 25 6e fe 8f f7  e1 be df f3 70 be 67 7d  |..4%n.......p.g}|
    000000d0: df be e7 7c ce 73 4b 73  18 eb 15 fe 2b 00 00 b0  |...|.sKs....+...|
    000000e0: 1a 19 42 ad 01 e0 82 3d  2d 56 62 a7 39 e0 c8 4f  |..B....=-Vb.9..O|
    000000f0: d2 96 06 17 51 ba 66 ba  00 50 f3 8a f9 d4 95 81  |....Q.f..P......|
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme$ binwalk --extract flag.png

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2858, uncompressed size: 3015, name: secret/flag.png
42897         0xA791          End of Zip archive, footer length: 22

srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme$ ls
_flag.png.extracted  flag.png
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme$ cd _flag.png.extracted/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme/_flag.png.extracted$ ls
29  29.zlib  9B3B.zip  secret
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme/_flag.png.extracted$ cd secret/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme/_flag.png.extracted/secret$ ls
flag.png
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme/_flag.png.extracted/secret$ eog flag.png
^C
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme/_flag.png.extracted/secret$ zsteg flag.png
meta date:create    .. text: "2023-03-16T02:01:55+00:00"
meta date:modify    .. [same as "meta date:create"]
imagedata           .. text: "KKZZ!!NN"
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/hideme/_flag.png.extracted/secret$
```

~~~
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_96539bea}
~~~


## Notas adicionales 

Checamos la imagen que se genero en secret después de usar `binwalk`

## Referencias
