## Descripción
A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message

Additional details will be available after launching your challenge instance.
Hints:
1. In the country that doesn't exist, the flag persists

## Solución 

Después de usar varias herramientas como `zsteg, eog, gimp`, usamos una herramienta llamada stepic.

```
SrRiv:~/SRSS/forensic/flags
>>> stepic -i upz.png -d
/usr/local/lib/python3.12/dist-packages/pillow-11.2.1-py3.12-linux-x86_64.egg/PIL/Image.py:3442: DecompressionBombWarning: Image size (150658990 pixels) exceeds limit of 89478485 pixels, could be decompression bomb DOS attack.
  warnings.warn(
picoCTF{fl4g_h45_fl4g1a2a9157}SrRiv:~/SRSS/forensic/flags
>>>
```

~~~
picoCTF{fl4g_h45_fl4g1a2a9157}
~~~


## Notas adicionales 

`stepic` es una herramienta de **esteganografía** en Linux, usada para **ocultar mensajes dentro de imágenes**, como archivos **png** .

## Referencias
