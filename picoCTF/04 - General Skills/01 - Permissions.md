## Descripción
Can you read files in the root file?

Hints:
1. What permissions do you have?

## Solución 
~~~
picoplayer@challenge:~$ sudo ls -la /root
Sorry, user picoplayer is not allowed to execute '/usr/bin/ls -la /root' as root on challenge.
picoplayer@challenge:~$ ls   
picoplayer@challenge:~$ ls /
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:~$ sudo vi

total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Mar 17 06:57 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile

Press ENTER or type command to continue
picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}

Press ENTER or type command to continue
ls: cannot open directory '/root': Permission denied

shell returned 2

Press ENTER or type command to continueConnection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
SrRiv-picoctf@webshell:~$
~~~
## Notas adicionales 
## Referencias