## Descripción
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/7/flag2of2-final.pdf).

Hints:
1. This problem can be solved by just opening the file in different ways
## Solución 
Abrimos el PDF y encontramos la parte final de la bandera:
```
1n_pn9_&_pdf_53b741d6}
```

Usamos una librería para convertir el pdf en png, para usar el comando convert se tiene que instalar `imagemagick` con el comando `sudo apt install imagemagick`:

```
SrRiv:~/SRSS/forensic/secretof
>>> convert flag2of2-final.pdf flag2of2-final.png
convert-im6.q16: profile 'icc': 'RGB ': RGB color space not permitted on grayscale PNG `flag2of2-final.png' @ warning/png.c/MagickPNGWarningHandler/1669.
SrRiv:~/SRSS/forensic/secretof
>>> ls
flag2of2-final.pdf  flag2of2-final.png
SrRiv:~/SRSS/forensic/secretof
>>> open flag2of2-final.png
```

Una vez abierta la imagen podremos completar la bandera:

~~~
picoCFT{f1u3n7_1n_pn9_&_pdf_53b741d6}
~~~


## Notas adicionales 

``

## Referencias
