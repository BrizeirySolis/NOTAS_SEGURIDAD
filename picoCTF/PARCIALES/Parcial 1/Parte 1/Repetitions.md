## Introducción
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/471/enc_flag).
1.-Multiple decoding is always good.
## Descripción
```

┌──(kali㉿kali)-[~/rep]
└─$ wget -4 https://artifacts.picoctf.net/c/471/enc_flag
--2024-11-26 21:33:30--  https://artifacts.picoctf.net/c/471/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: ‘enc_flag’

enc_flag             100%[=====================>]     349  --.-KB/s    in 0s      

2024-11-26 21:33:31 (258 MB/s) - ‘enc_flag’ saved [349/349]

                                                                                   
┌──(kali㉿kali)-[~/rep]
└─$ ls
enc_flag
                                                                                   
┌──(kali㉿kali)-[~/rep]
└─$ cat enc_flag                  
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFpSV0VKWVZGVmtNRTVHV2tWU2JYUlVDbUpXV25sVWJGcHZWbGRHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
                                                                                   
┌──(kali㉿kali)-[~/rep]
└─$ $ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
$: command not found
                                                                                   
┌──(kali㉿kali)-[~/rep]
└─$ $ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d
$: command not found
                                                                                   
┌──(kali㉿kali)-[~/rep]
└─$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}
                                                      
```

## Solución 
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_9b59b35c}