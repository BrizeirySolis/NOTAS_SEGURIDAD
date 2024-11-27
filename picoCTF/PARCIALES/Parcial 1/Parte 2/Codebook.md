## Introducción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)
1.- On the webshell, use `ls` to see if both files are in the directory you are in
2.-The `str_xor` function does not need to be reverse engineered for this challenge.
## Descripción
```
┌──(kali㉿kali)-[~/code]
└─$ wget -4 https://artifacts.picoctf.net/c/1/codebook.txt
--2024-11-26 22:26:39--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: ‘codebook.txt’

codebook.txt         100%[=====================>]      27  --.-KB/s    in 0s      

2024-11-26 22:26:40 (11.0 MB/s) - ‘codebook.txt’ saved [27/27]

                                                                                   
┌──(kali㉿kali)-[~/code]
└─$ ls
codebook.txt  code.py
                                                                                   
┌──(kali㉿kali)-[~/code]
└─$ cat codebook.txt                              
azbycxdwevfugthsirjqkplomn
                                                                                   
┌──(kali㉿kali)-[~/code]
└─$ python3 code.oy   
python3: can't open file '/home/kali/code/code.oy': [Errno 2] No such file or directory
                                                                                   
┌──(kali㉿kali)-[~/code]
└─$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}

```

## Solución 
picoCTF{c0d3b00k_455157_d9aa2df2}