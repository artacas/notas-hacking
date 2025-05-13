## Descripción:
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/110/enc_flag).

Hints:
Engaging in various decoding processes is of utmost importance
## Solución:
```
                                                                                                                                                                                                                                         
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://artifacts.picoctf.net/c_titan/110/enc_flag                                      
--2025-05-13 15:03:17--  https://artifacts.picoctf.net/c_titan/110/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.61, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag                                                   100%[========================================================================================================================================>]      73  --.-KB/s    in 0s      

2025-05-13 15:03:18 (131 MB/s) - ‘enc_flag’ saved [73/73]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ cat enc_flag 
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzJhMnd6TW1zeWZRPT0nCg==
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ echo YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzJhMnd6TW1zeWZRPT0nCg== | base64 -d
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg2a2wzMmsyfQ=='

Al texto b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg2a2wzMmsyfQ==' le quito la b y las comillas

┌──(kali㉿kali)-[~/Documents]
└─$ echo d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg2a2wzMmsyfQ== | base64 -d                        
wpjvJAM{jhlzhy_k3jy9wa3k_86kl32k2}    

y después se decodifica con el Cifrado Caesar con la llave 3

picoCTF{caesar_d3cr9pt3d_86de32d2}
```

## Notas:


