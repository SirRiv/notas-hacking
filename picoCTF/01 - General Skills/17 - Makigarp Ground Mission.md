## Descripción
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin. Login via `ssh` as `ctf-player` with the password, `6dee9772`
Additional details will be available after launching your challenge instance.

Hints:
1. Finding a cheatsheet for bash would be really helpful!
## Solución
```

ctf-player@pico-chall$ pwd
/home/ctf-player/drop-in
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ 
ctf-player@pico-chall$ ^C
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  boot  etc   instructions-to-3of3.txt  lib64  mnt  proc  run   srv  tmp  var
bin            dev   home  lib                       media  opt  root  sbin  sys  usr
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_\/\/4t3r_
ctf-player@pico-chall$ 

ctf-player@pico-chall$ cd $HOME
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
540e4e79}
ctf-player@pico-chall$ 

picoCTF{xxsh_0ut_0f_\/\/4t3r_540e4e79}

```

## Notas adicionales

## Referencias

