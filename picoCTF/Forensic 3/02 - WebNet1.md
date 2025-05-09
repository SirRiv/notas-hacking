## Descripción

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

Hints:
1. Try using a tool like Wireshark.
2. How can you decrypt the TLS stream?
## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet1$ wireshark capture.pcap &
[1] 1537
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet1$  ** (wireshark:1537) 12:33:41.887402 [GUI CRITICAL] -- Failed to create wl_display (No such file or directory)
nl80211 not found.
^C
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet1$ ls
capture.pcap  picopico.key  vulture.jpg
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet1$ eog vulture.jpg
^C
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet1$ string vulture.jpg | grep picoCTF
Command 'string' not found, did you mean:
  command 'strings' from deb binutils (2.42-4ubuntu2.4)
  command 'spring' from deb ruby-spring (2.1.1-2)
  command 'spring' from deb spring (106.0+dfsg-3)
Try: sudo apt install <deb name>
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet1$ strings vulture.jpg | grep picoCTF
picoCTF{honey.roasted.peanuts}
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/webnet1$
~~~

`picoCTF{honey.roasted.peanuts}`

## Notas adicionales 

Usamos la key para observar los paquetes, descargamos una imagen de uno de esos paquetes. Dicha imagen contiene la bandera. Y con strings podemos buscarla.
## Referencias
