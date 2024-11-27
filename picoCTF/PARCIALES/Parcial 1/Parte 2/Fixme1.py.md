## Introducción
Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)

1.-Indentation is very meaningful in Python
2.-To view the file in the webshell, do: `$ nano fixme1.py`
3.-To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4.-The `str_xor` function does not need to be reverse engineered for this challenge.
## Descripción
```

┌──(kali㉿kali)-[~/fx1]
└─$ wget -4 https://artifacts.picoctf.net/c/26/fixme1.py    
--2024-11-26 22:38:24--  https://artifacts.picoctf.net/c/26/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.64, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: ‘fixme1.py’

fixme1.py            100%[=====================>]     837  --.-KB/s    in 0s      

2024-11-26 22:38:25 (10.8 MB/s) - ‘fixme1.py’ saved [837/837]

                                                                                   
┌──(kali㉿kali)-[~/fx1]
└─$ python3 fixme1.py
  File "/home/kali/fx1/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
                                                                                   
┌──(kali㉿kali)-[~/fx1]
└─$ nano fixme1.py  
                                                                                   
┌──(kali㉿kali)-[~/fx1]
└─$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
                                                                           
```

## Solución 
picoCTF{1nd3nt1ty_cr1515_09ee727a}