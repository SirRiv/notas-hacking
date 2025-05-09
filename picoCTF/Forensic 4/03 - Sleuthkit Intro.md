## Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.


## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Sleuthkit$ wget https://artifacts.picoctf.net/c/164/disk.img.gz
--2025-05-08 12:34:21--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.61, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz                       100%[==========================================================>]  28.34M  6.49MB/s    in 6.5s

2025-05-08 12:34:29 (4.37 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Sleuthkit$ gzip -d disk.img.gz
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Sleuthkit$ ls -lah disk.img
-rw-r--r-- 1 srriv srriv 100M Aug  4  2023 disk.img
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Sleuthkit$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Sleuthkit$ nc saturn.picoctf.net 51573
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
~~~

`picoCTF{mm15_f7w!}`
## Notas adicionales 

``
## Referencias
