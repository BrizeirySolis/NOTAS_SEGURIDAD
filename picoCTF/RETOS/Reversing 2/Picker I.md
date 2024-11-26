## Introducción
This service can provide you with a random number, but can it do anything else?Connect to the program with netcat:`$ nc saturn.picoctf.net 61394`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/513/picker-I.py).

1.-Can you point the program to a function that does something useful for you?
## Descripción
![[Pasted image 20241126002123.png]]

```
┌──(kali㉿kali)-[~/p1]
└─$ wget https://artifacts.picoctf.net/c/513/picker-I.py
--2024-11-26 01:20:15--  https://artifacts.picoctf.net/c/513/picker-I.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 2600:9000:25ed:e400:16:5ec5:2840:93a1, 2600:9000:25ed:8400:16:5ec5:2840:93a1, 2600:9000:25ed:3e00:16:5ec5:2840:93a1, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|2600:9000:25ed:e400:16:5ec5:2840:93a1|:443... ^C
                                                                               
┌──(kali㉿kali)-[~/p1]
└─$ wget -4 https://artifacts.picoctf.net/c/513/picker-I.py
--2024-11-26 01:20:34--  https://artifacts.picoctf.net/c/513/picker-I.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.64, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3429 (3.3K) [application/octet-stream]
Saving to: ‘picker-I.py’

picker-I.py         100%[==================>]   3.35K  --.-KB/s    in 0s      

2024-11-26 01:20:35 (62.7 MB/s) - ‘picker-I.py’ saved [3429/3429]

                                                                               
┌──(kali㉿kali)-[~/p1]
└─$ nc saturn.picoctf.net 61394
Try entering "getRandomNumber" without the double quotes...
==> win
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x5f 0x64 0x31 0x34 0x6d 0x30 0x6e 0x64 0x5f 0x31 0x6e 0x5f 0x37 0x68 0x33 0x5f 0x72 0x30 0x75 0x67 0x68 0x5f 0x62 0x35 0x32 0x33 0x62 0x32 0x61 0x31 0x7d 
Try entering "getRandomNumber" without the double quotes...
==> 


```
## Solución 
picoCTF{4_d14m0nd_1n_7h3_r0ugh_b523b2a1}