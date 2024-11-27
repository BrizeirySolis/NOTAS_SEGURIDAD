## Introducción
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 60920

1.-ASCII is one of the most common encodings used in programming
2.-We know that the glitch output is valid Python, somehow!
3.-Press Ctrl and c on your keyboard to close your connection and return to the command prompt.
## Descripción
```

┌──(kali㉿kali)-[~]
└─$ nc saturn.picoctf.net 60920
'picoCTF{gl17ch_m3_n07_' + chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) + '}'
                                                                                   
┌──(kali㉿kali)-[~]
└─$ python3 script.py       
  File "/home/kali/script.py", line 1
    flag_glitch_cat = chr(0x62) + chr(0x64) + chr(0x61) + chr(0x36) + chr(0x38) + chr(0x66) + chr(0x37) + chr(0x35) 
IndentationError: unexpected indent
                                                                                   
┌──(kali㉿kali)-[~]
└─$ nano script.py             
                                                                                   
┌──(kali㉿kali)-[~]
└─$ python3 script.py
picoCTF{gl17ch_m3_n07_bda68f75}
                                                                                   
┌──(kali㉿kali)-[~]
└─$ 




```
## Solución 
picoCTF{gl17ch_m3_n07_bda68f75}