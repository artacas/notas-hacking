## Descripción:
A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their messageTry it [here](http://standard-pizzas.picoctf.net:61173/)!

Hints:
In the country that doesn't exist, the flag persists
## Solución:
```
┌──(kali㉿kali)-[~/Documents]
└─$ stepic upz.png                    
usage: stepic [-h] [--version] [--debug] [-d] [-e] [-f FORMAT] [-i FILE] [-t FILE] [-o FILE]
stepic: error: unrecognized arguments: upz.png
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ stepic -d -i upz.png -o flag.txt
/home/kali/.local/share/pipx/venvs/stepic/lib/python3.13/site-packages/PIL/Image.py:3442: DecompressionBombWarning: Image size (150658990 pixels) exceeds limit of 89478485 pixels, could be decompression bomb DOS attack.
  warnings.warn(

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ 
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ cat flag.txt 
picoCTF{fl4g_h45_fl4g00518d32}                                                                                                                                                                                                                                            
```

## Notas:
En el codigo fuente en la bandera UPZ decia importante

