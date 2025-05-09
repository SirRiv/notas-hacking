## Descripción
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

Additional details will be available after launching your challenge instance.

## Solución 

~~~
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ gzip disk.img.gz
gzip: disk.img.gz already has .gz suffix -- unchanged
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ gzip -d disk.img.gz
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ ls
disk.img
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ ls -la disk.img
-rw-r--r-- 1 srriv srriv 241172480 Aug  4  2023 disk.img
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ fls disk.img -o 206848
d/d 458:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 79: proc
d/d 80: dev
d/d 81: tmp
d/d 82: lib
d/d 85: var
d/d 94: usr
d/d 104:        bin
d/d 118:        sbin
d/d 464:        media
d/d 468:        mnt
d/d 469:        opt
d/d 470:        root
d/d 471:        run
d/d 473:        srv
d/d 474:        sys
V/V 33049:      $OrphanFiles
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ fls disk.img -o 206848 470
r/r 2344:       .ash_history
d/d 3916:       .ssh
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ fls disk.img -o 206848 3916
r/r 2345:       id_ed25519
r/r 2346:       id_ed25519.pub
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ icat disk.img -o 206848 2345 > key_file
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ chmod 600 key_file
srriv@LAPTOP-7DDM83G8:~/SRSS/forensic/operationOni$ ssh -i key_file -p 59271 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:59271 ([13.59.203.175]:59271)' can't be established.
ED25519 key fingerprint is SHA256:XBSvB1lk28EctsAVdKJtsl0A7C5bonqPrvHCYH8aEy4.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:59271' (ED25519) to the list of known hosts.
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

ctf-player@challenge:~$ ls
flag.txt
ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_af277f77}
~~~

`picoCTF{k3y_5l3u7h_af277f77}`



## Notas adicionales 


## Referencias
