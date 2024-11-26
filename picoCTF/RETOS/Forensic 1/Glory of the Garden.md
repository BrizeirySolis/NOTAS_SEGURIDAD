## Introducción
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

1.- What is a hex editor?
## Descripción
  ```
  ┌──(kali㉿kali)-[~/glory]
└─$ wget -4 https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
--2024-11-25 20:01:42--  https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg          100%[==================>]   2.19M   781KB/s    in 2.9s    

2024-11-25 20:01:45 (781 KB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                               
┌──(kali㉿kali)-[~/glory]
└─$ strings garden.jpg |grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"
                                                                               
┌──(kali㉿kali)-[~/glory]
└─$ 

```
## Solución 
picoCTF{more_than_m33ts_the_3y33dd2eEF5}