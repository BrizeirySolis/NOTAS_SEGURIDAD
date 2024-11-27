## Introducción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/10/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/10/level1.flag.txt.enc) in the same directory too.

1.-To view the file in the webshell, do: `$ nano level1.py`
2.-To exit `nano`, press Ctrl and x and follow the on-screen prompts.
3.-The `str_xor` function does not need to be reverse engineered for this challenge.
## Descripción
```
└─$ wget -4 https://artifacts.picoctf.net/c/10/level1.py    
--2024-11-26 23:13:26--  https://artifacts.picoctf.net/c/10/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: ‘level1.py’

level1.py            100%[=====================>]     876  --.-KB/s    in 0s      

2024-11-26 23:13:26 (56.3 MB/s) - ‘level1.py’ saved [876/876]

                                                                                   
┌──(kali㉿kali)-[~/pw1]
└─$ wget -4 https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
--2024-11-26 23:13:36--  https://artifacts.picoctf.net/c/10/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: ‘level1.flag.txt.enc’

level1.flag.txt.enc  100%[=====================>]      30  --.-KB/s    in 0s      

2024-11-26 23:13:36 (13.7 MB/s) - ‘level1.flag.txt.enc’ saved [30/30]

                                                                                   
┌──(kali㉿kali)-[~/pw1]
└─$ ls              
level1.flag.txt.enc  level1.py
                                                                                   
┌──(kali㉿kali)-[~/pw1]
└─$ nano level1.py  
                                                                                   
┌──(kali㉿kali)-[~/pw1]
└─$ python3 level1.py
Please enter correct password for flag: 691d
Welcome back... your flag, user:

picoCTF{545h_r1ng1ng_56891419}
```

## Solución 
picoCTF{545h_r1ng1ng_56891419}