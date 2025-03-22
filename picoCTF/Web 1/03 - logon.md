## Descripción
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796
Hints:
1. Hmm it doesn't seem to check anyone's password, except for Joe's?
## Solución 

~~~
picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}
~~~
## Notas adicionales 

En este problema se tenía que acceder al sitio como otro usuario que no fuese Joe, se analizó la Cookie y descubrimos que existe la posibilidad de cambiar la Cookie para ser administradores, una vez que se realizó la modificación de la Cookie se puede acceder a la solución del reto.

## Referencias
