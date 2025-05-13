## Descripción:
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext).

Hints:
caesar cipher [tutorial](https://learncryptography.com/classical-encryption/caesar-cipher)
## Solución:
```
                                                                                                                                                                                                                                        
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext
--2025-05-13 14:23:20--  https://jupiter.challenges.picoctf.org/static/6385b895dcb30c74dbd1f0ea271e3563/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext                                                 100%[========================================================================================================================================>]      35  --.-KB/s    in 0s      

2025-05-13 14:23:20 (81.2 MB/s) - ‘ciphertext’ saved [35/35]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ cat ciphertext 
picoCTF{dspttjohuifsvcjdpoabrkttds}                 

en CyberChef usando el algoritmo de ROT13 25 veces

picoCTF{crossingtherubiconzaqjsscr}  
```

