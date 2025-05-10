## Descripción:
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/f63e4eba644c99e92324b65cbd875db6/dds1-alpine.flag.img.gz)

Hints:
- Have you ever used `file` to determine what a file was?
- Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
- Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
- Using your own computer, you could use qemu to boot from this disk!
## Solución:
```
                                                                                                                               
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://mercury.picoctf.net/static/f63e4eba644c99e92324b65cbd875db6/dds1-alpine.flag.img.gz
--2025-05-08 14:24:58--  https://mercury.picoctf.net/static/f63e4eba644c99e92324b65cbd875db6/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img.gz         100%[=======================================================>]  28.39M   655KB/s    in 77s     

2025-05-08 14:26:24 (376 KB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]

                                                                                                                                
┌──(kali㉿kali)-[~/Documents]
└─$ gzip -d dds1-alpine.flag.img.gz 
                                                                                                                                
┌──(kali㉿kali)-[~/Documents]
└─$ ls
dds1-alpine.flag.img
                                                                                                                                
┌──(kali㉿kali)-[~/Documents]
└─$ file dds1-alpine.flag.img 
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
                                                                                                                                
┌──(kali㉿kali)-[~/Documents]
└─$ srch_strings dds1-alpine.flag.img | grep picoCTF
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_ad5c96c0}

```

## Notas:


