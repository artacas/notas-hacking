## Descripción:
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static)? This [BASH script](https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh) might help!

Hints:
None

## Solución:
```
artacas-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static
--2025-02-15 19:15:31--  https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: 'static'

static                                                    100%[==================================================================================================================================>]   8.18K  --.-KB/s    in 0s      

2025-02-15 19:15:31 (223 MB/s) - 'static' saved [8376/8376]

artacas-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh
--2025-02-15 19:15:56--  https://mercury.picoctf.net/static/e9dd71b5d11023873b8abe99cdb45551/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: 'ltdis.sh'

ltdis.sh                                                  100%[==================================================================================================================================>]     785  --.-KB/s    in 0s      

2025-02-15 19:15:57 (300 MB/s) - 'ltdis.sh' saved [785/785]
artacas-picoctf@webshell:~$ chmod +x ltdis.sh
artacas-picoctf@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
artacas-picoctf@webshell:~$ grep "picoCTF" static.ltdis.strings.txt
   1020 picoCTF{d15a5m_t34s3r_ae0b3ef2}
```