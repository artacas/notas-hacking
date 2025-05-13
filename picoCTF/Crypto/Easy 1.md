## Descripción:
The one time pad can be cryptographically secure, but not when you know the key. Can you solve this? We've given you the encrypted flag, key, and a table to help `UFJKXQZQUNB` with the key of `SOLVECRYPTO`. Can you use this [table](https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt) to solve it?.

Hints:
- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{HELLO}' as the flag.
- Please use all caps for the message.
## Solución:
```
                                                                                                                                                                                                                                        
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt 
--2025-05-13 14:28:57--  https://jupiter.challenges.picoctf.org/static/1fd21547c154c678d2dab145c29f1d79/table.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1571 (1.5K) [application/octet-stream]
Saving to: ‘table.txt’

table.txt                                                  100%[========================================================================================================================================>]   1.53K  --.-KB/s    in 0s      

2025-05-13 14:28:58 (63.9 MB/s) - ‘table.txt’ saved [1571/1571]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ cat table.txt 
    A B C D E F G H I J K L M N O P Q R S T U V W X Y Z 
   +----------------------------------------------------
A | A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
B | B C D E F G H I J K L M N O P Q R S T U V W X Y Z A
C | C D E F G H I J K L M N O P Q R S T U V W X Y Z A B
D | D E F G H I J K L M N O P Q R S T U V W X Y Z A B C
E | E F G H I J K L M N O P Q R S T U V W X Y Z A B C D
F | F G H I J K L M N O P Q R S T U V W X Y Z A B C D E
G | G H I J K L M N O P Q R S T U V W X Y Z A B C D E F
H | H I J K L M N O P Q R S T U V W X Y Z A B C D E F G
I | I J K L M N O P Q R S T U V W X Y Z A B C D E F G H
J | J K L M N O P Q R S T U V W X Y Z A B C D E F G H I
K | K L M N O P Q R S T U V W X Y Z A B C D E F G H I J
L | L M N O P Q R S T U V W X Y Z A B C D E F G H I J K
M | M N O P Q R S T U V W X Y Z A B C D E F G H I J K L
N | N O P Q R S T U V W X Y Z A B C D E F G H I J K L M
O | O P Q R S T U V W X Y Z A B C D E F G H I J K L M N
P | P Q R S T U V W X Y Z A B C D E F G H I J K L M N O
Q | Q R S T U V W X Y Z A B C D E F G H I J K L M N O P
R | R S T U V W X Y Z A B C D E F G H I J K L M N O P Q
S | S T U V W X Y Z A B C D E F G H I J K L M N O P Q R
T | T U V W X Y Z A B C D E F G H I J K L M N O P Q R S
U | U V W X Y Z A B C D E F G H I J K L M N O P Q R S T
V | V W X Y Z A B C D E F G H I J K L M N O P Q R S T U
W | W X Y Z A B C D E F G H I J K L M N O P Q R S T U V
X | X Y Z A B C D E F G H I J K L M N O P Q R S T U V W
Y | Y Z A B C D E F G H I J K L M N O P Q R S T U V W X
Z | Z A B C D E F G H I J K L M N O P Q R S T U V W X Y

con este código de Python:
alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"  
key = "SOLVECRYPTO"  
encrypted_flag = "UFJKXQZQUNB"  
  
def modular_subtraction(encrypted_flag):  
res = ""  
for i in range(len(encrypted_flag)):  
if (ord(encrypted_flag[i]) - ord(key[i])) >= 0:  
res += chr(ord(encrypted_flag[i]) - ord(key[i]) + 65)  
else:  
res += chr(ord(encrypted_flag[i]) - ord(key[i]) + 91)  
return res  
  
print("And the flag is: picoCTF{" + modular_subtraction(encrypted_flag) + "}")

arroja la bandera:

                                                                                                                                                                                                                               
┌──(kali㉿kali)-[~/Documents]
└─$ python3 xd.py
And the flag is: picoCTF{CRYPTOISFUN}

```

## Notas:
El código decripta mensajes con el Cifrado Vernam