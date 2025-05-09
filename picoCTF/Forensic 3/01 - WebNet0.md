## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
Hints:
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?
## Solución 

```srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet0$ wireshark capture.pcap &
[1] 991
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet0$  ** (wireshark:991) 12:17:49.151492 [GUI CRITICAL] -- Failed to create wl_display (No such file or directory)
nl80211 not found.
^C
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet0$

```

~~~
picoCTF{nongshim.shrimp.crackers}
~~~


## Notas adicionales 

Usamos Wireshark para abrir el archivo .pcap, luego con el archivo .key desbloqueamos algunos paquetes. Usamos Ctrl + F para buscar dentro de los detalles del paquete para buscar el inicio `picoCTF`

## Referencias
