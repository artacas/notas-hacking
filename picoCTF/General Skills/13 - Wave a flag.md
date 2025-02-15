## Descripción:
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm) has extraordinarily helpful information...

Hints:
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm`
- Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.

## Solución:
```
artacas-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
--2025-02-15 19:13:01--  https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                                      100%[==================================================================================================================================>]  10.68K  --.-KB/s    in 0s      

2025-02-15 19:13:01 (182 MB/s) - 'warm' saved [10936/10936]

artacas-picoctf@webshell:~$ chmod +x warm
artacas-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
artacas-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
```