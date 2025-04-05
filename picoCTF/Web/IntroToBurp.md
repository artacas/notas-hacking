## Descripción:
Try [here](http://titan.picoctf.net:57544/) to find the flag

Hints:
- Try using burpsuite to intercept request to capture the flag.
- Try mangling the request, maybe their server-side code doesn't handle malformed requests very well.
## Solución:
```
picoCTF{#0TP_Bypvss_SuCc3$S_6bffad21}
```

## Notas:
Con BurpSuite intercepté la solicitud del OTP y la modifiqué quitándole el otp= y me regresó la bandera