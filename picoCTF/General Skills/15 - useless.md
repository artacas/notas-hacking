## Descripción:
There's an interesting script in the user's home directory

Additional details will be available after launching your challenge instance.

The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.

```
Hostname: saturn.picoctf.net
Port:     64261
Username: picoplayer
Password: password
```

Hints:
None

## Solución:
```
artacas-picoctf@webshell:~$ ssh saturn.picoctf.net -p 64261 -l picoplayer
The authenticity of host '[saturn.picoctf.net]:64261 ([13.59.203.175]:64261)' can't be established.
ED25519 key fingerprint is SHA256:DiJcS90U9QussLS8HLR6l6BGJb5eCA0vRmA18IvDvw8.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:64261' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ ls
useless
picoplayer@challenge:~$ man useless

useless
     useless, -- This is a simple calculator script

SYNOPSIS
     useless, [add sub mul div] number1 number2

DESCRIPTION
     Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.

Examples
     ./useless add 1 2
       This will add 1 and 2 and return 3

     ./useless mul 2 3
       This will return 6 as a product of 2 and 3

     ./useless div 6 3
       This will return 2 as a quotient of 6 and 3

     ./useless sub 6 5
       This will return 1 as a remainder of substraction of 5 from 6

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_8504}

picoplayer@challenge:~$ Connection to saturn.picoctf.net closed by remote host.
Connection to saturn.picoctf.net closed.
```