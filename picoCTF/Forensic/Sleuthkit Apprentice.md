## Descripción:
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)

Hints:
None
## Solución:
```
                                                                                                                         
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://artifacts.picoctf.net/c/136/disk.flag.img.gz
--2025-05-08 14:37:05--  https://artifacts.picoctf.net/c/136/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534571 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz                100%[=======================================================>]  45.33M  10.0MB/s    in 5.6s    

2025-05-08 14:37:19 (8.14 MB/s) - ‘disk.flag.img.gz’ saved [47534571/47534571]

                                                                                                     
┌──(kali㉿kali)-[~/Documents]
└─$ gzip -d disk.flag.img.gz 

                                                                                                  
┌──(kali㉿kali)-[~/Documents]
└─$ mmls disk.flag.img  
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)

                                                                                                                 
┌──(kali㉿kali)-[~/Documents]
└─$ fls disk.flag.img -o 360448 -r | grep flag
++ r/r * 2082(realloc): flag.txt
++ r/r 2371:    flag.uni.txt
                                                                                                                                
┌──(kali㉿kali)-[~/Documents]
└─$ icat disk.flag.img -o 360448 2371
picoCTF{by73_5urf3r_3497ae6b}


```

## Notas:


