## Introducción
http://mercury.picoctf.net:48380/
Look at the problem category

## Descripción
```
                                                                               
┌──(kali㉿kali)-[~/Milkslap]
└─$ wget -4 http://mercury.picoctf.net:48380/concat_v.png
--2024-11-24 23:01:26--  http://mercury.picoctf.net:48380/concat_v.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:48380... connected.
HTTP request sent, awaiting response... 200 OK
Length: 18095920 (17M) [image/png]
Saving to: ‘concat_v.png’

concat_v.png        100%[==================>]  17.26M  8.39MB/s    in 2.1s    

2024-11-24 23:01:29 (8.39 MB/s) - ‘concat_v.png’ saved [18095920/18095920]

                                                                               
┌──(kali㉿kali)-[~/Milkslap]
└─$ zsteg -a concat_v.png | grep pico                    
b1,b,lsb,xy         .. text: "picoCTF{imag3_m4n1pul4t10n_sl4p5}\n"

```

## Solución 
picoCTF{imag3_m4n1pul4t10n_sl4p5}