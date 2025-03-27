## Descripción
Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:21485/](http://mercury.picoctf.net:21485/)
## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS$ for i in {1..30} ; do curl -s http://mercury.picoctf.net:21485/check -H "Cookie: name=$i"; don
e | grep "picoCTF{"
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}</code></p>
srriv@LAPTOP-7DDM83G8:~/SRSS$

picoCTF{3v3ry1_l0v3s_c00k135_94190c8a}
~~~
## Notas adicionales 

## Referencias
