## Introducción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.

1.-Does that encoding look familiar?
2.-The `str_xor` function does not need to be reverse engineered for this challenge.
## Descripción
```
- `chr(0x64)` → ASCII character for hex `0x64` is **'d'**.
- `chr(0x65)` → ASCII character for hex `0x65` is **'e'**.
- `chr(0x37)` → ASCII character for hex `0x37` is **'7'**.
- `chr(0x36)` → ASCII character for hex `0x36` is **'6'**.
zsh: corrupt history file /home/kali/.zsh_history
┌──(kali㉿kali)-[~]
└─$ cd pw2
                                                                                   
┌──(kali㉿kali)-[~/pw2]
└─$ ls
level2.flag.txt.enc  level2.flag.txt.enc.1  level2.py  level2.py.1
                                                                                   
┌──(kali㉿kali)-[~/pw2]
└─$ nano level2,py  
                                                                                   
┌──(kali㉿kali)-[~/pw2]
└─$ python3 level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}

```
## Solución 
picoCTF{tr45h_51ng1ng_489dea9a}