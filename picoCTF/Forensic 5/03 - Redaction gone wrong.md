## Descripción
Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

Hints:
1. How can you be sure of the redaction?
## Solución 

```
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Redaction$ wget https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
--2025-05-18 22:46:55--  https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.61, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Report_for_ABC_Labs.pdf 100%[==========================================================>]  34.10K  --.-KB/s    in 0.04s

2025-05-18 22:46:55 (778 KB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]

srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/Redaction$ xdg-open Financial_Report_for_ABC_Labs.pdf
```

Una vez abierto el reporte en libreoffice. Empece a mover los cuadros que tapaban el texto en el documento y ahi se encontraba la bandera.

~~~
picoCTF{C4n_Y0u_S33_m3_fully}
~~~


## Notas adicionales 

``

## Referencias
