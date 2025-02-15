## Descripción:
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/502/files.zip)

Hints:
None

## Solución:
```
artacas-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/502/files.zip
--2025-02-15 19:49:41--  https://artifacts.picoctf.net/c/502/files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3995553 (3.8M) [application/octet-stream]
Saving to: 'files.zip'

files.zip                                                 100%[==================================================================================================================================>]   3.81M  1.80MB/s    in 2.1s    

2025-02-15 19:49:43 (1.80 MB/s) - 'files.zip' saved [3995553/3995553]

artacas-picoctf@webshell:~$ unzip files.zip 
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
artacas-picoctf@webshell:~$ cd files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
artacas-picoctf@webshell:~/files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets$ cat uber-secret.txt 
picoCTF{f1nd_15_f457_ab443fd1}
```