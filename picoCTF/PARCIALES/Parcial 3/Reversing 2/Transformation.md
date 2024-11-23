## Introducción
I wonder what this really is... [enc](https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`

You may find some decoders online
## Descripción
Como el mensaje es en algun idioma, buscamos atravez de un pequeño programa para obtenerlas en hexadecimal y asi obtener su codigo ascii

```
                                                                           
┌──(kali㉿kali)-[~]
└─$ wget https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc
--2024-11-22 21:49:36--  https://mercury.picoctf.net/static/0d3145dafdc4fbcf01891912eb6c0968/enc
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 57 [application/octet-stream]
Saving to: ‘enc’

enc                100%[===============>]      57  --.-KB/s    in 0s      

2024-11-22 21:49:36 (23.1 MB/s) - ‘enc’ saved [57/57]

                                                                           
┌──(kali㉿kali)-[~]
└─$ cat enc                       
灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸弲㘶㠴挲ぽ                                                                           
┌──(kali㉿kali)-[~]
└─$ python          
Python 3.11.9 (main, Apr 10 2024, 13:16:36) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> for c in enc:
...     print(hex(ord(c)).lstrip("0x"),end='')
... 
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'enc' is not defined
>>> enc= open("enc").read()
>>> for c in enc:
...     print(hex(ord(c)).lstrip("0x"),end='')
... 
7069636f4354467b31365f626974735f696e73743334645f6f665f385f32363638346332307>>> 
KeyboardInterrupt                                                            
>>> 

```

https://www.rapidtables.com/convert/number/hex-to-ascii.html

7069636f4354467b31365f626974735f696e73743334645f6f665f385f32363638346332307
## Solución 
picoCTF{16_bits_inst34d_of_8_26684c20}