## Descripción:
A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/960abba2fdbc9be5013ef87f1df67213e9b63d4561d7a8c8c1ce7a4ce40a547e/myNetworkTraffic.pcap) and try to get the flag.

Hints:
- Filter your packets to narrow down your search.
- Attacks were done in timely manner.
- Time is essential
## Solución:
```
                                                                                                                                                                                  
┌──(kali㉿kali)-[~/Documents]
└─$ wget https://challenge-files.picoctf.net/c_verbal_sleep/960abba2fdbc9be5013ef87f1df67213e9b63d4561d7a8c8c1ce7a4ce40a547e/myNetworkTraffic.pcap
--2025-05-12 22:40:50--  https://challenge-files.picoctf.net/c_verbal_sleep/960abba2fdbc9be5013ef87f1df67213e9b63d4561d7a8c8c1ce7a4ce40a547e/myNetworkTraffic.pcap
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 65.9.149.59, 65.9.149.85, 65.9.149.24, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|65.9.149.59|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1452 (1.4K) [application/octet-stream]
Saving to: ‘myNetworkTraffic.pcap’

myNetworkTraffic.pcap                                      100%[========================================================================================================================================>]   1.42K  --.-KB/s    in 0s      

2025-05-12 22:40:50 (53.1 MB/s) - ‘myNetworkTraffic.pcap’ saved [1452/1452]

                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ wireshark myNetworkTraffic.pcap                                                                                                               
 ** (wireshark:25963) 22:42:05.709777 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::SystemPalette
 ** (wireshark:25963) 22:42:05.711311 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::ToolButtonPalette
 ** (wireshark:25963) 22:42:05.711691 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::ButtonPalette
 ** (wireshark:25963) 22:42:05.712014 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::CheckBoxPalette
 ** (wireshark:25963) 22:42:05.712180 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::RadioButtonPalette
 ** (wireshark:25963) 22:42:05.712234 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::HeaderPalette
 ** (wireshark:25963) 22:42:05.712334 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::ItemViewPalette
 ** (wireshark:25963) 22:42:05.712409 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::MessageBoxLabelPelette
 ** (wireshark:25963) 22:42:05.712503 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::TabBarPalette
 ** (wireshark:25963) 22:42:05.712598 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::LabelPalette
 ** (wireshark:25963) 22:42:05.712670 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::GroupBoxPalette
 ** (wireshark:25963) 22:42:05.712763 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::MenuPalette
 ** (wireshark:25963) 22:42:05.712856 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::MenuBarPalette
 ** (wireshark:25963) 22:42:05.712995 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::TextEditPalette
 ** (wireshark:25963) 22:42:05.713120 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::TextEditPalette
 ** (wireshark:25963) 22:42:05.713170 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::TextLineEditPalette
 ** (wireshark:25963) 22:42:05.713252 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::ToolTipPalette
 ** (wireshark:25963) 22:42:05.713396 [GUI ECHO] -- virtual QVariant Qt6CTPlatformTheme::themeHint(QPlatformTheme::ThemeHint) const
 ** (wireshark:25963) 22:42:05.713926 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::SystemPalette
 ** (wireshark:25963) 22:42:06.116938 [GUI ECHO] -- virtual QVariant Qt6CTPlatformTheme::themeHint(QPlatformTheme::ThemeHint) const
 ** (wireshark:25963) 22:42:06.261536 [GUI ECHO] -- virtual const QPalette* Qt6CTPlatformTheme::palette(QPlatformTheme::Palette) const QPlatformTheme::SystemPalette
zsh: segmentation fault  wireshark myNetworkTraffic.pcap
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents]
└─$ tshark -r myNetworkTraffic.pcap -x
0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 d0 0a 00 00 42 4e 41 55 64 36 55 3d   P. .....BNAUd6U=

Frame (52 bytes):
0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 05 5b 00 00 65 7a 46 30 58 33 63 30   P. ..[..ezF0X3c0
0030  63 77 3d 3d                                       cw==
Reassembled TCP (12 bytes):
0000  42 4e 41 55 64 36 55 3d 63 77 3d 3d               BNAUd6U=cw==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 9c db 00 00 6e 30 74 6e 34 6a 59 3d   P. .....n0tn4jY=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 71 03 00 00 59 5a 59 41 76 45 73 3d   P. .q...YZYAvEs=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 fd 41 00 00 63 47 6c 6a 62 30 4e 55   P. ..A..cGljb0NU
0030  52 67 3d 3d                                       Rg==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 73 c6 00 00 68 57 69 55 76 71 51 3d   P. .s...hWiUvqQ=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 f6 5a 00 00 58 7a 4d 30 63 33 6c 66   P. ..Z..XzM0c3lf
0030  64 41 3d 3d                                       dA==

0000  45 00 00 2c 00 01 00 00 40 06 f8 76 c0 a8 00 02   E..,....@..v....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 69 97 00 00 66 51 3d 3d               P. .i...fQ==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 6d eb 00 00 67 56 73 52 6f 50 55 3d   P. .m...gVsRoPU=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 7c f1 00 00 77 32 69 52 48 6e 67 3d   P. .|...w2iRHng=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 1b 0d 00 00 59 6d 68 66 4e 48 4a 66   P. .....YmhfNHJf
0030  5a 51 3d 3d                                       ZQ==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 ae d0 00 00 6f 5a 59 72 50 47 45 3d   P. .....oZYrPGE=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 da a7 00 00 2b 5a 79 68 38 7a 55 3d   P. .....+Zyh8zU=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 a1 f2 00 00 32 46 6c 6a 55 41 77 3d   P. .....2FljUAw=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 67 c1 00 00 7a 33 49 79 7a 76 67 3d   P. .g...z3Iyzvg=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 15 65 00 00 4e 57 55 34 59 7a 63 34   P. ..e..NWU4Yzc4
0030  5a 41 3d 3d                                       ZA==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 52 f1 00 00 67 43 6a 76 79 39 6f 3d   P. .R...gCjvy9o=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 84 e9 00 00 47 36 55 7a 74 4a 77 3d   P. .....G6UztJw=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 ef ae 00 00 35 68 37 66 39 67 77 3d   P. .....5h7f9gw=

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 a7 c8 00 00 4c 70 50 75 51 36 77 3d   P. .....LpPuQ6w=

0000  45 00 00 34 00 01 00 00 40 06 f8 6e c0 a8 00 02   E..4....@..n....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 eb 52 00 00 62 6e 52 66 64 47 67 30   P. ..R..bnRfdGg0
0030  64 41 3d 3d                                       dA==

0000  45 00 00 30 00 01 00 00 40 06 f8 72 c0 a8 00 02   E..0....@..r....
0010  c0 a8 01 02 00 14 00 50 00 00 00 00 00 00 00 00   .......P........
0020  50 02 20 00 d5 01 00 00 51 48 45 53 48 47 59 3d   P. .....QHESHGY=

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_e5e8c78d}
```

## Notas:
Fui poniendo parte por parte lo que parecia que era texto en base 64 en CyberChef para pasar de base64 a texto normal (primero los tuve que ordenar por tiempo)

