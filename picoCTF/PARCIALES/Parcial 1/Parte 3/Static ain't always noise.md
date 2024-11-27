## Introducción
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static)? This [BASH script](https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh) might help!

## Descripción
```
┌──(kali㉿kali)-[~/sAN]
└─$ wget -4 https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
--2024-11-27 00:29:03--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/static
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 8376 (8.2K) [application/octet-stream]
Saving to: ‘static’

static               100%[=====================>]   8.18K  --.-KB/s    in 0s      

2024-11-27 00:29:03 (175 MB/s) - ‘static’ saved [8376/8376]

                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ wget -4 https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
--2024-11-27 00:29:19--  https://mercury.picoctf.net/static/0f6ea599582dcce7b4f1ba94e3617baf/ltdis.sh
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 785 [application/octet-stream]
Saving to: ‘ltdis.sh’

ltdis.sh             100%[=====================>]     785  --.-KB/s    in 0s      

2024-11-27 00:29:20 (14.8 MB/s) - ‘ltdis.sh’ saved [785/785]

                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ ls
ltdis.sh  static
                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ chmod +x static
                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ chmod +x warm  
chmod: cannot access 'warm': No such file or directory
                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ la 
ltdis.sh  static
                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ strings static | grep pico
picoCTF{d15a5m_t34s3r_6f8c8200}

```
## Solución 
picoCTF{d15a5m_t34s3r_6f8c8200}