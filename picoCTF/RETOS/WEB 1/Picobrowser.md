## Introducción
This website can be rendered only by **picobrowser**, go and catch the flag! `https://jupiter.challenges.picoctf.org/problem/28921/` ([link](https://jupiter.challenges.picoctf.org/problem/28921/)) or http://jupiter.challenges.picoctf.org:28921

You don't need to download a new web browser
## Descripción
User-Agent:
es un request header es una cadena que le permite al servidor identificarse,segun el navegador.

curl  -s https://jupiter.challenges.picoctf.org/problem/28921/flag -H "user-Agent:picobrowser" | grep pico

![[Pasted image 20241121234429.png]]
## Solución 

picoCTF{p1c0_s3cr3t_ag3nt_84f9c865}