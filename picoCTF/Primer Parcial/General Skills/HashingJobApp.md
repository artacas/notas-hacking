## Descripción:
If you want to hash with the best, beat this test!`nc saturn.picoctf.net 59544`

Hints:
- You can use a commandline tool or web app to hash text
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

## Solución:
```
artacas-picoctf@webshell:~$ nc saturn.picoctf.net 59544
Please md5 hash the text between quotes, excluding the quotes: 'chorus girls'
Answer: 
fdaf7298de6707185d68175ba4bd2f17    
fdaf7298de6707185d68175ba4bd2f17
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'chimpanzees'
Answer: 
e5ab2ced9d181b61fec5d2c5c20a9de0
e5ab2ced9d181b61fec5d2c5c20a9de0
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'local police'
Answer: 
b36e4003adb9138e0c7f0379b9be4d5b
b36e4003adb9138e0c7f0379b9be4d5b
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_3eb82b73}
```

## Notas:
Usé CyberChef con la receta de MD5

