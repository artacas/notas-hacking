## Descripción:
Help us test the form by submiting the username as `test` and password as `test!`The website running [here](http://saturn.picoctf.net:52543/).

Hints:
any redirections?

## Solución:
```
picoCTF{proxies_all_the_way_d1c0b112}
```

## Notas:
En el navegador en inspeccionar elemento en network le di en preserve log y al momento de iniciar sesión con los datos que se dan se genera algo que dice id=cGljb0NURntwcm94aWVzX2Fs y otro que dice id=bF90aGVfd2F5X2QxYzBiMTEyfQ== que al decodificarlos de base64 da la bandera
