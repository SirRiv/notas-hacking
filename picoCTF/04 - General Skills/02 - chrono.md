## Descripción
How to automate tasks to run at intervals on linux servers?
Additional details will be available after launching your challenge instance.
## Solución 

~~~
SrRiv-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 58056
The authenticity of host '[saturn.picoctf.net]:58056 ([13.59.203.175]:58056)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:58056' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
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

picoplayer@challenge:~$ chrono -h
-bash: chrono: command not found
picoplayer@challenge:~$ chron -h
-bash: chron: command not found
picoplayer@challenge:~$ ls
picoplayer@challenge:~$ ls /
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:~$ ls /etc
adduser.conf            cron.d          default       group-       init.d        libaudit.conf  mailcap.order        os-release  rc0.d        rmt       subgid       terminfo
alternatives            cron.daily      deluser.conf  gshadow      inputrc       localtime      mime.types           pam.conf    rc1.d        security  subgid-      timezone
apt                     cron.hourly     dhcp          gshadow-     issue         login.defs     mke2fs.conf          pam.d       rc2.d        selinux   subuid       tmpfiles.d
bash.bashrc             cron.monthly    dpkg          gss          issue.net     logrotate.d    modules-load.d       passwd      rc3.d        shadow    subuid-      ucf.conf
bindresvport.blacklist  cron.weekly     e2scrub.conf  host.conf    kernel        lsb-release    mtab                 passwd-     rc4.d        shadow-   sudoers      ufw
binfmt.d                crontab         environment   hostname     ld.so.cache   machine-id     networkd-dispatcher  profile     rc5.d        shells    sudoers.d    update-motd.d
ca-certificates         dbus-1          fstab         hosts        ld.so.conf    magic          networks             profile.d   rc6.d        skel      sysctl.conf  wgetrc
ca-certificates.conf    debconf.conf    gai.conf      hosts.allow  ld.so.conf.d  magic.mime     nsswitch.conf        python3     rcS.d        ssh       sysctl.d     xattr.conf
cloud                   debian_version  group         hosts.deny   legal         mailcap        opt                  python3.8   resolv.conf  ssl       systemd      xdg
picoplayer@challenge:~$ grep "picoCTF" cri
.bash_logout  .bashrc       .cache/       .profile      
picoplayer@challenge:~$ grep "picoCTF" /etc/crontab 
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
picoplayer@challenge:~$ cron
cron: can't open or create /var/run/crond.pid: Permission denied
picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
SrRiv-picoctf@webshell:~$


picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}

~~~
## Notas adicionales 
## Referencias
