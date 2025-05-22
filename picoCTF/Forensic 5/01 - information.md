## Descripción
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/149ab4b27d16922142a1e8381677d76f/cat.jpg)
Hints:
1. Look at the details of the file
2. Make sure to submit the flag as picoCTF{XXXXX}
## Solución 

```
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/information$ exiftool cat.jpg
ExifTool Version Number         : 12.76
File Name                       : cat.jpg
Directory                       : .
File Size                       : 878 kB
File Modification Date/Time     : 2021:03:15 12:24:46-06:00
File Access Date/Time           : 2025:05:18 22:25:31-06:00
File Inode Change Date/Time     : 2025:05:18 22:24:40-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/information$ echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d
picoCTF{the_m3tadata_1s_modified}srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/information$
```

~~~
picoCTF{the_m3tadata_1s_modified}
~~~


## Notas adicionales 

Observamos en los metadatos que la `License` es una cadena que podría ser base 64, la decodificamos con un comando y obtenemos la bandera 
## Referencias
