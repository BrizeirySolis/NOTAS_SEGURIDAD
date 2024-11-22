## Introducción
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? https://jupiter.challenges.picoctf.org/problem/15796/

Hmm it doesn't seem to check anyone's password, except for Joe's?
## Descripción
HTTP : protocolo de capa de aplicación para documentos hypermedia  como html para comunicación de navegador y servidor, cliente abre navegador haciendo request hasta recibir un response. 

Headers: pasan información adicional con la petición http.

Request headers: encabezados para pedirle al servidor información, con método GET y la respuesta tiene código de 200 

cookie: bloque de datos grabado mientras un usuario navega
instalando el editor de cookie vamos y editamos en admin el valor de false por true y eso nos da la bandera

![[Pasted image 20241122131733.png]]
o desde consola 

curl https://jupiter.challenges.picoctf.org/problem/15796/flag -H "Cookie: username=admin; password=hola; admin=True; " | grep pico
![[Pasted image 20241122131956.png]]
## Solución 

picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}