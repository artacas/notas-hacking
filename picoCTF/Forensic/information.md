## Descripción:
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/e5825f58ef798fdd1af3f6013592a971/cat.jpg)

Hints:
- Look at the details of the file
- Make sure to submit the flag as picoCTF{XXXXX}
## Solución:
```
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://mercury.picoctf.net/static/e5825f58ef798fdd1af3f6013592a971/cat.jpg
--2025-05-12 21:55:06--  https://mercury.picoctf.net/static/e5825f58ef798fdd1af3f6013592a971/cat.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 878136 (858K) [application/octet-stream]
Saving to: ‘cat.jpg’

cat.jpg                                                    100%[========================================================================================================================================>] 857.55K  2.56MB/s    in 0.3s    

2025-05-12 21:55:07 (2.56 MB/s) - ‘cat.jpg’ saved [878136/878136]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ file cat.jpg 
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
picoCTF{the_m3tadata_1s_modified}         


```

## Notas:
En los metadatos en la parte de licencia estaba la bandera en base64

