## Introducción
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!

## Descripción
````
┌──(kali㉿kali)-[~/pages]
└─$ wget https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt
--2024-11-25 22:24:27--  https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2976 (2.9K) [application/octet-stream]
Saving to: ‘whitepages.txt’

whitepages.txt      100%[==================>]   2.91K  --.-KB/s    in 0s      

2024-11-25 22:24:28 (60.9 MB/s) - ‘whitepages.txt’ saved [2976/2976]

                                                                               
┌──(kali㉿kali)-[~/pages]
└─$ xxd whitepages.txt | head
00000000: e280 83e2 8083 e280 83e2 8083 20e2 8083  ............ ...
00000010: 20e2 8083 e280 83e2 8083 e280 83e2 8083   ...............
00000020: 20e2 8083 e280 8320 e280 83e2 8083 e280   ...... ........
00000030: 83e2 8083 20e2 8083 e280 8320 e280 8320  .... ...... ... 
00000040: 2020 e280 83e2 8083 e280 83e2 8083 e280    ..............
00000050: 8320 20e2 8083 20e2 8083 e280 8320 e280  .  ... ...... ..
00000060: 8320 20e2 8083 e280 83e2 8083 2020 e280  .  .........  ..
00000070: 8320 20e2 8083 2020 2020 e280 8320 e280  .  ...    ... ..
00000080: 83e2 8083 e280 83e2 8083 2020 e280 8320  ..........  ... 
00000090: e280 8320 e280 8320 e280 83e2 8083 e280  ... ... ........
                                                                               
┌──(kali㉿kali)-[~/pages]
└─$  python3 -m pip install pwntools

┌──(kali㉿kali)-[~/pages]
└─$ nano exp.py     
                                                                               
┌──(kali㉿kali)-[~/pages]
└─$ python exp.py   
b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}\n\t\t'
                                                                               
┌──(kali㉿kali)-[~/pages]
└─$ 

```
## Solución 
icoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}\