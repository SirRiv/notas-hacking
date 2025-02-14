## Descripción
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.
Hints:
1. Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.
## Solución 
Cyberchef

```
Input: bDNhcm5fdGgzX3IwcDM1
Recipe: From base 64
Output: l3arn_th3_r0p35

picoCTF{l3arn_th3_r0p35}
```

## Solución 2
Python
```
SrRiv-picoctf@webshell:~$ python     
Python 3.10.12 (main, Sep 11 2024, 15:47:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import base64
>>> base64.b64decode('bDNhcm5fdGgzX3IwcDM1')
b'l3arn_th3_r0p35'
>>>
picoCTF{l3arn_th3_r0p35}
```
## Notas adicionales 
## Referencias
