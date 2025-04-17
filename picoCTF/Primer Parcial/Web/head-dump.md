## Descripción:
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag.The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden.The website is running [picoCTF News](http://verbal-sleep.picoctf.net:63482/).

Hints:
- Explore backend development with us
- The head was dumped.

## Solución:
```
picoCTF{Pat!3nt_15_Th3_K3y_8635db4b}
```

## Notas:
En la página que da, en la parte de API Documentation hasta abajo donde dice heapdump al darle en ejecutar da la opción de descargar un archivo, que haciendole grep se encuentra la bandera (lo hice con un comando de windows llamado findstr que funciona igual que el grep)

