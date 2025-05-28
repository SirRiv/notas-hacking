## Descripción
Do you know how to use the web inspector?

Additional details will be available after launching your challenge instance.
Hints:
1. Use the web inspector on other files included by the web page.
2. The flag may or may not be encoded

## Solución 
~~~
picoCTF{web_succ3ssfully_d3c0ded_10f9376f}
~~~
## Notas adicionales 

Comenzamos a navegar en todos los apartados de la pagina, al inspeccionar podemos visualizar dentro de `About Us`, en la etiqueta `<section>` una elemento que podría ser base 64, con ello podemos realizar una conversión con CyberChef y obtener la bandera.

## Referencias
