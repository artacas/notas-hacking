## Descripción:
Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:21939/](http://mercury.picoctf.net:21939/)

Hints:
- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses

## Solución:
```
artacas-picoctf@webshell:~$ curl -I http://mercury.picoctf.net:21939/index.php
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_6ef27873}
Content-type: text/html; charset=UTF-8

artacas-picoctf@webshell:~$ 
```
