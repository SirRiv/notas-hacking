## Descripción
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/37821/` ([link](https://jupiter.challenges.picoctf.org/problem/37821/)) or http://jupiter.challenges.picoctf.org:37821
Hints: 
1. Never trust the client
## Solución 
~~~
picoCTF{no_clients_plz_1a3c89}
~~~
## Notas adicionales 

En este reto tenemos que acceder mediante la contraseña en una pagina web, no contamos con la contraseña, pero una vez analizamos con Ctrl + U, podemos observar que en el mismo HTML hace una validación con If para determinar si la contraseña es correcta, una vez armamos la contraseña entera se obtuvo la flag.
## Referencias
