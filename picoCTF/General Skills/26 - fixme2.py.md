## Descripción:
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

Hints:
- Are equality and assignment the same symbol?
- To view the file in the webshell, do: `$ nano fixme2.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución:
```
artacas-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/6/fixme2.py
--2025-02-21 03:12:55--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                                 100%[==================================================================================================================================>]   1.00K  --.-KB/s    in 0s      

2025-02-21 03:12:55 (526 MB/s) - 'fixme2.py' saved [1029/1029]

artacas-picoctf@webshell:~$ python3 fixme2.py 
  File "/home/artacas-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
artacas-picoctf@webshell:~$ nano fixme2.py 
artacas-picoctf@webshell:~$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

## Notas:
Le faltaba un = en una comparacion de un if