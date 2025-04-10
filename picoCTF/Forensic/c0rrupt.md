## Descripción:
We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag.

Hints:
Try fixing the file header

## Solución:
```
                                                                                                                                                                                                                                          
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
--2025-04-09 23:43:01--  https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 202940 (198K) [application/octet-stream]
Saving to: ‘mystery’

mystery                                                    100%[=======================================================================================================================================>] 198.18K  1.13MB/s    in 0.2s    

2025-04-09 23:43:02 (1.13 MB/s) - ‘mystery’ saved [202940/202940]

                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Documents]
└─$ xxd -g 1 mystery | head
00000000: 89 65 4e 34 0d 0a b0 aa 00 00 00 0d 43 22 44 52  .eN4........C"DR
00000010: 00 00 06 6a 00 00 04 47 08 02 00 00 00 7c 8b ab  ...j...G.....|..
00000020: 78 00 00 00 01 73 52 47 42 00 ae ce 1c e9 00 00  x....sRGB.......
00000030: 00 04 67 41 4d 41 00 00 b1 8f 0b fc 61 05 00 00  ..gAMA......a...
00000040: 00 09 70 48 59 73 aa 00 16 25 00 00 16 25 01 49  ..pHYs...%...%.I
00000050: 52 24 f0 aa aa ff a5 ab 44 45 54 78 5e ec bd 3f  R$......DETx^..?
00000060: 8e 64 cd 71 bd 2d 8b 20 20 80 90 41 83 02 08 d0  .d.q.-.  ..A....
00000070: f9 ed 40 a0 f3 6e 40 7b 90 23 8f 1e d7 20 8b 3e  ..@..n@{.#... .>
00000080: b7 c1 0d 70 03 74 b5 03 ae 41 6b f8 be a8 fb dc  ...p.t...Ak.....
00000090: 3e 7d 2a 22 33 6f de 5b 55 dd 3d 3d f9 20 91 88  >}*"3o.[U.==. ..
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Documents]
└─$ printf '\x89\x50\x4E\x47\x0D\x0A\x1A\x0A' | dd of=mystery bs=1 seek=0 count=8 conv=notrunc

8+0 records in
8+0 records out
8 bytes copied, 8.6658e-05 s, 92.3 kB/s
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Documents]
└─$ printf '\x49\x48\x44\x52' | dd of=mystery bs=1 seek=12 count=4 conv=notrunc

4+0 records in
4+0 records out
4 bytes copied, 0.00010001 s, 40.0 kB/s
                                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/Documents]
└─$ printf 'IDAT' | dd of=mystery bs=1 seek=87 count=4 conv=notrunc

4+0 records in
4+0 records out
4 bytes copied, 0.00010853 s, 36.9 kB/s

picoCTF{c0rrupt10n_1847995}

```

## Notas:
El header estaba corrupto, se tuvo que arreglar con algunos comandos para después poder abrir la imagen donde estaba la bandera. El archivo era .png