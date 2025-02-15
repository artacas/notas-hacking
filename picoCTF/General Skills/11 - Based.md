## Descripción
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.

Hints:
- I hear python can convert things.
- It might help to have multiple windows open.

## Solución:
```
artacas-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29956
Let us see how data is stored
map
Please give the 01101101 01100001 01110000 as a word.
...
you have 45 seconds.....

Input:
map
Please give me the  154 151 155 145 as a word.
Input:
lime
Please give me the 70656172 as a word.
Input:
pear
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_b375bb16}
```

## Notas:
Todos los números fueron transformados con CyberChef