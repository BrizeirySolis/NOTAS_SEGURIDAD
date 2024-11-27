## Introducción
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
1.-[strings](https://linux.die.net/man/1/strings)
## Descripción
```
└─$ wget -4 https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
--2024-11-27 00:36:55--  https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: ‘strings’

strings              100%[=====================>] 757.84K  1.96MB/s    in 0.4s    

2024-11-27 00:36:56 (1.96 MB/s) - ‘strings’ saved [776032/776032]

                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ strings strings | grep "picoCTF{"
picoCTF{5tRIng5_1T_7f766a23}
                                                                                   
┌──(kali㉿kali)-[~/sAN]
└─$ 


```

## Solución 
picoCTF{5tRIng5_1T_7f766a23}