## Descripción:
[🥛](http://mercury.picoctf.net:58537/)

Hints:
Look at the problem category

## Solución:
```
┌──(kali㉿kali)-[~/Documents]
└─$ wget http://mercury.picoctf.net:58537/concat_v.png
--2025-05-10 11:15:01--  http://mercury.picoctf.net:58537/concat_v.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:58537... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18095920 (17M) [image/png]
Saving to: ‘concat_v.png’

concat_v.png                                               100%[========================================================================================================================================>]  17.26M  8.51MB/s    in 2.0s    

2025-05-10 11:15:03 (8.51 MB/s) - ‘concat_v.png’ saved [18095920/18095920]

┌──(kali㉿kali)-[~/Documents]
└─$ zsteg concat_v.png | grep picoCTF

picoCTF{imag3_m4n1pul4t10n_sl4p5}
```

## Notas:


