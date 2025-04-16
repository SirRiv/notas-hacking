## Descripción
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
Hints:
1. How did pictures from the moon landing get sent back to Earth?
2. What is the CMU mascot?, that might help select a RX option

## Solución 

Con la herramienta SSTV:

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/m00nwalk$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [###################################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
srriv@LAPTOP-7DDM83G8:~/SRSS/m00nwalk$
~~~

Finalmente abrimos la imagen, en la cual podemos observar la bandera.

~~~
picoCTF{beep_boop_im_in_space}
~~~
## Notas adicionales 
## Referencias
