## Descripción:
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)

Hints:
- Indentation is very meaningful in Python
- To view the file in the webshell, do: `$ nano fixme1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución:
```
artacas-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2025-02-21 03:07:06--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.42, 3.160.5.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                                 100%[==================================================================================================================================>]     837  --.-KB/s    in 0s      

2025-02-21 03:07:06 (70.4 MB/s) - 'fixme1.py' saved [837/837]

artacas-picoctf@webshell:~$ python fixme1.py 
  File "/home/artacas-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
artacas-picoctf@webshell:~$ nano fixme1.py 
artacas-picoctf@webshell:~$ nano fixme1.py 
artacas-picoctf@webshell:~$ python fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
```

## Notas:
Marcaba error porque la identacion de la linea estaba mal