## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

## Solución 

Visualizamos con wireshark que la mayoría son UDP entonces realizamos un seguimiento, en cierto Stream podemos visualizar un inicio y un final, ahi podemos observar que todos los paquetes son enviados de un puerto >5000 a un puerto 22. Y que el numero de puerto de origen es el numero de caracter ascii para forjar la bandera.

~~~
Ether / IP / UDP 10.0.0.66:5000 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5112 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5105 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5099 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5111 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5067 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5084 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5070 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5123 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5112 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5049 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5076 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5076 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5102 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5051 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5114 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5051 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5100 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5095 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5100 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5097 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5116 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5097 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5095 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5118 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5049 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5097 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5095 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5115 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5116 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5051 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5103 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5048 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.66:5125 > 10.0.0.1:22 / Raw / Padding
Ether / IP / UDP 10.0.0.80:5000 > 10.0.0.1:22 / Raw / Padding

~~~

Creamos un codigo en python

~~~
from scapy.all import *

packets = rdpcap('capture.pcap')

flag = ""

for p in packets:
        if UDP in p and p[UDP].dport==22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)
~~~

Y imprimimos el resultado
~~~
(venv) srriv@LAPTOP-7DDM83G8:~/SRSS/shark/shark2$ python3 exp.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}
~~~

~~~
picoCTF{p1LLf3r3d_data_v1a_st3g0}
~~~


## Notas adicionales 
## Referencias
