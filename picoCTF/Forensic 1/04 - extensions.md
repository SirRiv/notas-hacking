## Descripción
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
Hints:
1. How do operating systems know what kind of file it is? (It's not just the ending!
2. Make sure to submit the flag as picoCTF{XXXXX}
## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/extensions$ mv flag.txt flag.pn
srriv@LAPTOP-7DDM83G8:~/SRSS/extensions$ mv flag.pn flag.png
srriv@LAPTOP-7DDM83G8:~/SRSS/extensions$ ls
flag.png
srriv@LAPTOP-7DDM83G8:~/SRSS/extensions$ eog flag.png



picoCTF{now_you_know_about_extensions}

~~~
## Notas adicionales 

Se analizó el archivo `flag.txt`, de esa manera pudimos observar que no era de tipo texto, sino que era una imagen, en mi caso realice un simple cambio de extensión para poder visualizar la imagen donde encontramos la bandera. Y con ayuda de la inteligencia artificial obtenemos el texto que se encuentra en la imagen.

## Referencias
