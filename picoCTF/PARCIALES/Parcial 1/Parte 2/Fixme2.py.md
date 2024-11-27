## Introducción

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
1.-Are equality and assignment the same symbol?
2.-To view the file in the webshell, do: `$ nano fixme2.py`
3.-To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4.-The `str_xor` function does not need to be reverse engineered for this challenge.
## Descripción
```
┌──(kali㉿kali)-[~/Desktop/picoctf/fix2]
└─$ wget -4 https://artifacts.picoctf.net/c/6/fixme2.py     
--2024-11-26 22:44:17--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: ‘fixme2.py’

fixme2.py            100%[=====================>]   1.00K  --.-KB/s    in 0s      

2024-11-26 22:44:17 (18.7 MB/s) - ‘fixme2.py’ saved [1029/1029]

                                                                                   
┌──(kali㉿kali)-[~/Desktop/picoctf/fix2]
└─$ python3 fixme.py              
python3: can't open file '/home/kali/Desktop/picoctf/fix2/fixme.py': [Errno 2] No such file or directory
                                                                                   
┌──(kali㉿kali)-[~/Desktop/picoctf/fix2]
└─$ python3 fixme2.py
  File "/home/kali/Desktop/picoctf/fix2/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
                                                                                   
┌──(kali㉿kali)-[~/Desktop/picoctf/fix2]
└─$ nano fixme2.py  
                                                                                   
┌──(kali㉿kali)-[~/Desktop/picoctf/fix2]
└─$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}

```

## Solución 
picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}