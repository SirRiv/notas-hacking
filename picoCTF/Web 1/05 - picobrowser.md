## Descripción
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/26704/` ([link](https://jupiter.challenges.picoctf.org/problem/26704/)) or http://jupiter.challenges.picoctf.org:26704

Hints:
1. You don't need to download a new web browser
## Solución 
~~~
picoCTF{p1c0_s3cr3t_ag3nt_e9b160d0
~~~
## Notas adicionales 

Al entrar en la pagina podemos observar que se requiere picobrowser para poder acceder a la bandera, cuando accedemos a un sitio se obtiene el nombre de nuestro navegador, lo cual es exactamente lo que no nos permite acceder al sitio, afortunadamente podemos realizar un cambio en la solicitud, y al cambiar el "User-Agent" a 'picobrowser' podemos obtener como el acceso a la bandera. 
## Referencias
