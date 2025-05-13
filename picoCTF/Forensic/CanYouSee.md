## Descripción:
How about some hide and seek?
Download this file [here](https://artifacts.picoctf.net/c_titan/130/unknown.zip).

Hints:
- How can you view the information about the picture?
- If something isn't in the expected form, maybe it deserves attention?
## Solución:
```
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://artifacts.picoctf.net/c_titan/130/unknown.zip 
--2025-05-12 22:23:19--  https://artifacts.picoctf.net/c_titan/130/unknown.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252265 (2.1M) [application/octet-stream]
Saving to: ‘unknown.zip’

unknown.zip                                                100%[========================================================================================================================================>]   2.15M  5.33MB/s    in 0.4s    

2025-05-12 22:23:21 (5.33 MB/s) - ‘unknown.zip’ saved [2252265/2252265]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ unzip unknown.zip  
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ exiftool ukn_reality.jpg                                     
ExifTool Version Number         : 13.10
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:11 20:05:55-04:00
File Access Date/Time           : 2025:05:12 22:23:27-04:00
File Inode Change Date/Time     : 2025:05:12 22:23:27-04:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ echo cGljb0NURntNRTc0RDQ3QV9ISUREM05fNmE5ZjVhYzR9Cg== | base64 -d
picoCTF{ME74D47A_HIDD3N_6a9f5ac4}
                                                   
```

## Notas:


