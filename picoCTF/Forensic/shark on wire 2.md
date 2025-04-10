## Descripción:
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.

Hints:
None

## Solución:
```
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```

## Notas:
Abrí el archivo `.pcap` con Wireshark y filtré los paquetes UDP desde la IP `10.0.0.66` al puerto `22`. Noté que los paquetes entre los que decían "start" y "end" tenían puertos de origen que empezaban con un 5, seguidos de tres dígitos. Tomé esos tres dígitos finales de cada puerto, los convertí a ASCII y reconstruí el mensaje carácter por carácter.