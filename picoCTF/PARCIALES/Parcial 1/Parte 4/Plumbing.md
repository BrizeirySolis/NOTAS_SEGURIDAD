## Introducción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.

1.-Remember the flag format is picoCTF{XXXX}
2.- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)
## Descripción
```
┌──(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 4427 |grep picoCTF
picoCTF{digital_plumb3r_5ea1fbd7}

```
## Solución 
picoCTF{digital_plumb3r_5ea1fbd7}