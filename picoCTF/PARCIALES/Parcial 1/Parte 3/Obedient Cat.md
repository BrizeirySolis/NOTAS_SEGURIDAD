## Introducción
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag).

1.-Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
2.-To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag`
3.-man cat
## Descripción
```
┌──(kali㉿kali)-[~/oc]
└─$ wget -4 https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
--2024-11-27 00:21:01--  https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: ‘flag’

flag                 100%[=====================>]      34  --.-KB/s    in 0s      

2024-11-27 00:21:02 (26.6 MB/s) - ‘flag’ saved [34/34]

                                                                                   
┌──(kali㉿kali)-[~/oc]
└─$ man cat 
                                                                                   
┌──(kali㉿kali)-[~/oc]
└─$ ls
flag
                                                                                   
┌──(kali㉿kali)-[~/oc]
└─$ cat flag                      
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}

```

## Solución 
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}