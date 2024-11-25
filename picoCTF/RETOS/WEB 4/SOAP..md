## Introducción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?[Web Portal](http://saturn.picoctf.net:51081/)

## Descripción
![[Pasted image 20241125004900.png]]

1.- Entrar a Burp 
2.-Activar proxy 
3.-Abrir Enlace De pico
4.- Seleccionar Burp en foxyproxy
5.-Abri enlace y dar clic en los 3 detaila
6.-Seleccionar un post 
7.-dar clic en send to repeater
8.- pegar la siguiente linea despues de utf-8 
https://book.hacktricks.xyz/pentesting-web/xxe-xee-xml-external-entity
<!DOCTYPE foo [<!ENTITY toreplace SYSTEM "/etc/passwd"> ]>

9.-precionar send 

## Solución 
picoCTF{XML_3xtern@l_3nt1t1ty_4dbeb2ed}