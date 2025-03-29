## Descripción:
Can you find the flag on this website.
Try to find the flag [here](http://saturn.picoctf.net:64469/).

Hints:
SQLiLite

## Solución:
```
picoCTF{G3tting_5QL_1nJ3c7I0N_l1k3_y0u_sh0ulD_c8b7cc2a}
```

Notas:
Con SQL Injection en la password, después en la busqueda se ingresó ' union select 1,id,flag from more_table;