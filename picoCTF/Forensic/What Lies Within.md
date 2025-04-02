## Descripción:
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

Hints:
There is data encoded somewhere... there might be an online decoder.

## Solución:
```                                                                                                  
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
--2025-04-01 14:56:41--  https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 625219 (611K) [application/octet-stream]
Saving to: ‘buildings.png’

buildings.png                                              100%[========================================================================================================================================>] 610.57K   703KB/s    in 0.9s    

2025-04-01 14:56:51 (703 KB/s) - ‘buildings.png’ saved [625219/625219]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ sudo gem install zsteg
[sudo] password for kali: 
Fetching zpng-0.4.5.gem
Fetching zsteg-0.2.13.gem
Fetching iostruct-0.5.0.gem
Fetching rainbow-3.1.1.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.5
Successfully installed iostruct-0.5.0
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.5.0
Installing ri documentation for iostruct-0.5.0
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 2 seconds
4 gems installed
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ xsteg -a buildings.png 
xsteg: command not found
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ zsteg -a buildings.png 
b1,r,lsb,xy         .. text: "^5>R5YZrG"
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"

picoCTF{h1d1ng_1n_th3_b1t5}
```

