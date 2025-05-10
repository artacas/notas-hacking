## Descripción:
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)

Hints:
None
## Solución:
```
                                                                                                                               
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://artifacts.picoctf.net/c/213/disk.flag.img.gz
--2025-05-08 14:55:10--  https://artifacts.picoctf.net/c/213/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 44360922 (42M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz                100%[=======================================================>]  42.31M  18.3MB/s    in 2.3s    

2025-05-08 14:55:21 (18.3 MB/s) - ‘disk.flag.img.gz’ saved [44360922/44360922]

                                                                                                                                
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
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)


```

## Notas:


