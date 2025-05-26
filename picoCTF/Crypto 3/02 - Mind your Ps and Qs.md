## Descripción
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values)

Hints:
1. Bits are expensive, I used only a little bit over 100 to save money
## Solución 
Tenemos los siguientes valores:
```
>>> cat values
Decrypt my super sick RSA:
c: 421345306292040663864066688931456845278496274597031632020995583473619804626233684
n: 631371953793368771804570727896887140714495090919073481680274581226742748040342637
e: 65537

```

En este caso usamos un factorizador para poder obtener p y q
Terminal Python:
```
SrRiv:~/SRSS/crypto/mind
>>> python3
Python 3.12.3 (main, Feb  4 2025, 14:48:35) [GCC 13.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> c = 421345306292040663864066688931456845278496274597031632020995583473619804626233684
>>> n= 631371953793368771804570727896887140714495090919073481680274581226742748040342637
>>> e = 65537
>>> p = 1461849912200000206276283741896701133693
>>> q= 431899300006243611356963607089521499045809
>>> p * q
631371953793368771804570727896887140714495090919073481680274581226742748040342637
>>> tn = (p-1)*(q-1)
>>> d = pow (e, -1, tn)
>>> m= pow(c, d, n)
>>> m
13016382529449106065927291425342535437996222135352905256639647889241102700065917
>>> bytes.fromhex(hex(m[2:])
...
...
... .
... .
  File "<stdin>", line 5
    .
    ^
SyntaxError: invalid syntax
>>> bytes.fromhex(hex(m)[2:])
b'picoCTF{sma11_N_n0_g0od_55304594}'
>>>
```

```
picoCTF{sma11_N_n0_g0od_55304594}
```
## Notas adicionales 


## Referencias
