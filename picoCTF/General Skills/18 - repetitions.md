## Descripción:
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/474/enc_flag).

Hints:
Multiple decoding is always good.

## Solución:
```
artacas-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/474/enc_flag
--2025-02-15 19:41:05--  https://artifacts.picoctf.net/c/474/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag                                                  100%[==================================================================================================================================>]     349  --.-KB/s    in 0s      

2025-02-15 19:41:05 (223 MB/s) - 'enc_flag' saved [349/349]

artacas-picoctf@webshell:~$ ls
README.txt  enc_flag
artacas-picoctf@webshell:~$ cat enc_flag 
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZhTTBKUFdXdGtlbVF4V2tkWGJYUllDbUY2UWpSWmEyaFRWakpHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==

Después en CyberChef le pasé eso y decodifiqué de base64 6 veces y me dio la bandera:

picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_3f81f7be}
```