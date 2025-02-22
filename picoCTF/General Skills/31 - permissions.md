## Descripción:
Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 57735 picoplayer@saturn.picoctf.net`Password: `vCR2tuwCRm`Can you login and read the root file?

Hints:
What permissions do you have?

## Solución:
```
artacas-picoctf@webshell:~$ ssh -p 57735 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:57735 ([13.59.203.175]:57735)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:57735' (ED25519) to the list of known hosts.
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

picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo vi

picoCTF{uS1ng_v1m_3dit0r_ad091ce1}
```

## Nota:
Usando el editor vi abri el archivo flag.txt que estaba en root/