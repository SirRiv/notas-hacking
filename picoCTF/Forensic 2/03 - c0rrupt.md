## Descripción

We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

Hints:
1. Try fixing the file header
## Solución 
Usamos Hexeditor para corregir los bytes del archivo png, y al solucionar podemos abrir la imagen y observar la bandera en la imagen.

~~~
Bytes iniciales de mystery.png:

00000000: 89 50 4E 47 0D 0A 1A 0A 00 00 00 0D 49 48 44 52
00000010: 00 00 00 66 00 00 00 47 08 02 00 00 00 7C 8B AB

00000040: 00 09 70 48 59 73 00 00 16 25 00 00 16 25 01 49
00000050: 52 24 F0 00 00 FF A5 49 44 41 54 78 5E EC BD 3F


~~~

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/c0rrupt$ hexeditor mystery
srriv@LAPTOP-7DDM83G8:~/SRSS/c0rrupt$ pngcheck -v mystery
zlib warning:  different version (expected 1.2.13, using 1.3)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
:  invalid chunk length (too large)
ERRORS DETECTED in mystery
srriv@LAPTOP-7DDM83G8:~/SRSS/c0rrupt$ hexeditor mystery
srriv@LAPTOP-7DDM83G8:~/SRSS/c0rrupt$ pngcheck -v mystery
zlib warning:  different version (expected 1.2.13, using 1.3)

File: mystery (202940 bytes)
  chunk IHDR at offset 0x0000c, length 13
    1642 x 1095 image, 24-bit RGB, non-interlaced
  chunk sRGB at offset 0x00025, length 1
    rendering intent = perceptual
  chunk gAMA at offset 0x00032, length 4: 0.45455
  chunk pHYs at offset 0x00042, length 9: 5669x5669 pixels/meter (144 dpi)
  chunk IDAT at offset 0x00057, length 65445
    zlib: deflated, 32K window, fast compression
  chunk IDAT at offset 0x10008, length 65524
  chunk IDAT at offset 0x20008, length 65524
  chunk IDAT at offset 0x30008, length 6304
  chunk IEND at offset 0x318b4, length 0
No errors detected in mystery (9 chunks, 96.3% compression).
srriv@LAPTOP-7DDM83G8:~/SRSS/c0rrupt$ mv mystery mystery.png
srriv@LAPTOP-7DDM83G8:~/SRSS/c0rrupt$

~~~

~~~
picoCTF{c0rrupt10n_1847995}
~~~
## Notas adicionales 
## Referencias
