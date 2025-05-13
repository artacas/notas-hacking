## Descripción:
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/97/flag2of2-final.pdf).

Hints:
This problem can be solved by just opening the file in different ways
## Solución:
```
                                                                                                                                                                                                                                        
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://artifacts.picoctf.net/c_titan/97/flag2of2-final.pdf
--2025-05-12 22:26:48--  https://artifacts.picoctf.net/c_titan/97/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: ‘flag2of2-final.pdf’

flag2of2-final.pdf                                         100%[========================================================================================================================================>]   3.28K  --.-KB/s    in 0s      

2025-05-12 22:26:49 (123 MB/s) - ‘flag2of2-final.pdf’ saved [3362/3362]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ file flag2of2-final.pdf 
flag2of2-final.pdf: PNG image data, 50 x 50, 8-bit/color RGBA, non-interlaced
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ cp flag2of2-final.pdf flag2of2-final.png 
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ binwalk flag2of2-final.pdf                    

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 50 x 50, 8-bit/color RGBA, non-interlaced
914           0x392           PDF document, version: "1.4"
1149          0x47D           Zlib compressed data, default compression

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ binwalk -e flag2of2-final.pdf

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
1149          0x47D           Zlib compressed data, default compression

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ cd _flag2of2-final.pdf.extracted 
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents/_flag2of2-final.pdf.extracted]
└─$ ls
47D  47D.zlib
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents/_flag2of2-final.pdf.extracted]
└─$ cat 47D                                                       
q 0.1 0 0 0.1 0 0 cm
0 g
q
10 0 0 10 0 0 cm BT
/R7 16 Tf
1 0 0 1 50 250 Tm
(1n_pn9_&_pdf_724b1287})Tj
ET
Q
Q

picoCTF{f1u3n7_1n_pn9_&_pdf_724b1287}
```

## Notas:
La primera parte de la bandera estaba en el archivo cambiando la extension a .png y la otra mitad adentro del archivo en un archivo llamado 47D

