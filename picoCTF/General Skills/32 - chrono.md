## Descripción:
How to automate tasks to run at intervals on linux servers?Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 58461
Username: picoplayer 
Password: ENAFb6zfzn
```

Hints:
None

## Solución:
```
artacas-picoctf@webshell:~$ ssh saturn.picoctf.net -p 58461 -l picoplayer
The authenticity of host '[saturn.picoctf.net]:58461 ([13.59.203.175]:58461)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:58461' (ED25519) to the list of known hosts.
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

picoplayer@challenge:~$ cd ../../
picoplayer@challenge:/$ ls
bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
picoplayer@challenge:/$ cd etc
picoplayer@challenge:/etc$ ls
adduser.conf            cloud         debconf.conf    fstab      hostname     kernel         logrotate.d    mke2fs.conf          pam.conf   rc0.d  resolv.conf  ssh        sysctl.conf  update-motd.d
alternatives            cron.d        debian_version  gai.conf   hosts        ld.so.cache    lsb-release    modules-load.d       pam.d      rc1.d  rmt          ssl        sysctl.d     wgetrc
apt                     cron.daily    default         group      hosts.allow  ld.so.conf     machine-id     mtab                 passwd     rc2.d  security     subgid     systemd      xattr.conf
bash.bashrc             cron.hourly   deluser.conf    group-     hosts.deny   ld.so.conf.d   magic          networkd-dispatcher  passwd-    rc3.d  selinux      subgid-    terminfo     xdg
bindresvport.blacklist  cron.monthly  dhcp            gshadow    init.d       legal          magic.mime     networks             profile    rc4.d  shadow       subuid     timezone
binfmt.d                cron.weekly   dpkg            gshadow-   inputrc      libaudit.conf  mailcap        nsswitch.conf        profile.d  rc5.d  shadow-      subuid-    tmpfiles.d
ca-certificates         crontab       e2scrub.conf    gss        issue        localtime      mailcap.order  opt                  python3    rc6.d  shells       sudoers    ucf.conf
ca-certificates.conf    dbus-1        environment     host.conf  issue.net    login.defs     mime.types     os-release           python3.8  rcS.d  skel         sudoers.d  ufw
picoplayer@challenge:/etc$ cat crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_1d781160}
picoplayer@challenge:/etc$ 
```

