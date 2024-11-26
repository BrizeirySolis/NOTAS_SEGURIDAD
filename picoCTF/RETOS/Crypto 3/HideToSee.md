## Introducción
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/239/atbash.jpg)
1.-Download the image and try to extract it.
## Descripción
```
┌──(kali㉿kali)-[~/hid]
└─$ wget -4 https://artifacts.picoctf.net/c/239/atbash.jpg 
--2024-11-25 18:48:42--  https://artifacts.picoctf.net/c/239/atbash.jpg
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.61, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 51504 (50K) [application/octet-stream]
Saving to: ‘atbash.jpg’

atbash.jpg          100%[==================>]  50.30K  --.-KB/s    in 0.09s   

2024-11-25 18:48:43 (546 KB/s) - ‘atbash.jpg’ saved [51504/51504]

                                                                               
┌──(kali㉿kali)-[~/hid]
└─$ open atbash.jpg
                       
```

* Subimos la imagen en: https://futureboy.us/stegano/decinput.html 
* Nos da el siguiente texto: krxlXGU{zgyzhs_xizxp_1u84w779}
* Copiamos el texto y lo mandamos a cyberchef atbash cypher: https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfMDV5Mno2NXp9&oenc=65001&ieol=CRLF

## Solución 
picoCTF{atbash_crack_1f84d779}