## Descripción

Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz)

Hints:
1. Have you ever used `file` to determine what a file was?
2. Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
3. Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
4. Using your own computer, you could use qemu to boot from this disk!
## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/disk$ wget https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz
--2025-05-08 12:25:03--  https://mercury.picoctf.net/static/4f3df7052b4121aff89af1a3f517afb1/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz           100%[==========================================================>]  28.39M   587KB/s    in 48s

2025-05-08 12:25:54 (606 KB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]

srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/disk$ ls -lah dds1-alpine.flag.img.gz
-rw-r--r-- 1 srriv srriv 29M Mar 15  2021 dds1-alpine.flag.img.gz
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/disk$ gzip -d dds1-alpine.flag.img.gz
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/disk$ ls -lah dds1-alpine.flag.img
-rw-r--r-- 1 srriv srriv 128M Mar 15  2021 dds1-alpine.flag.img
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/disk$ file dds1-alpine.flag.img
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/disk$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/disk$
~~~

`picoCTF{f0r3ns1c4t0r_n30phyt3_a011c142}`

## Notas adicionales 

``
## Referencias
