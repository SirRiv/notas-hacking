## Descripción
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/1/challenge.zip)

Additional details will be available after launching your challenge instance.

Hints:
1. QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
2. Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
3. If you don't have access to a phone, you can also use zbar-tools to convert an image to text

## Solución 

```
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise$ unzip challenge.zip
Archive:  challenge.zip
   creating: home/ctf-player/drop-in/
 extracting: home/ctf-player/drop-in/flag.png
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise$ ls
challenge.zip  home
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise$ cd home/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise/home$ ls
ctf-player
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise/home$ cd ctf-player/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise/home/ctf-player$ ls
drop-in
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise/home/ctf-player$ cd drop-in/
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise/home/ctf-player/drop-in$ ls
flag.png
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/ScanSurpise/home/ctf-player/drop-in$ zbarimg flag.png
QR-Code:picoCTF{p33k_@_b00_3f7cf1ae}
scanned 1 barcode symbols from 1 images in 0 seconds
```

~~~
picoCTF{p33k_@_b00_3f7cf1ae}
~~~


## Notas adicionales 

Usamos `zbarimg` para escanear el codigo QR que nos da el challenge. De esta manera obtenemos la bandera.
## Referencias
