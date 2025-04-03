## Descripción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
Hints:
1. Try using a tool like Wireshark
2. What are streams?
	
## Solución 

Usando Wireshark:

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/Whatarestreams$ wireshark capture.pcap
~~~

![[Pasted image 20250401124435.png]]

![[Pasted image 20250401124503.png]]

~~~
picoCTF{StaT31355_636f6e6e}
~~~

## Notas adicionales 

Se abrió el archivo en wireshark para identificar los patrones de trafico en el paquete. Se realizó una investigación de los streams para identificar la información intercambiada, y en uno se encontró la bandera.

## Referencias
