## Descripción
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/129/unknown.zip).
Hints:
1. How can you view the information about the picture?
2. If something isn't in the expected form, maybe it deserves attention?

## Solución 

```srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/CanYouSee$ wget https://artifacts.picoctf.net/c_titan/129/unknown.zip
--2025-05-18 23:25:52--  https://artifacts.picoctf.net/c_titan/129/unknown.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252200 (2.1M) [application/octet-stream]
Saving to: ‘unknown.zip’

unknown.zip                       100%[==========================================================>]   2.15M  6.09MB/s    in 0.4s

2025-05-18 23:25:53 (6.09 MB/s) - ‘unknown.zip’ saved [2252200/2252200]

srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/CanYouSee$ file unknown.zip
unknown.zip: Zip archive data, at least v2.0 to extract, compression method=deflate
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/CanYouSee$ unzip unknown.zip
Archive:  unknown.zip
  inflating: ukn_reality.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/CanYouSee$ ls
ukn_reality.jpg  unknown.zip
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/CanYouSee$ exiftool ukn_reality.jpg
ExifTool Version Number         : 12.76
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:11 18:05:53-06:00
File Access Date/Time           : 2024:03:11 18:05:53-06:00
File Inode Change Date/Time     : 2025:05:18 23:26:07-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/CanYouSee$ echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==" | base64 -d
picoCTF{ME74D47A_HIDD3N_b32040b8}
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/CanYouSee$

```

~~~
picoCTF{ME74D47A_HIDD3N_b32040b8}
~~~


## Notas adicionales 

``

## Referencias
