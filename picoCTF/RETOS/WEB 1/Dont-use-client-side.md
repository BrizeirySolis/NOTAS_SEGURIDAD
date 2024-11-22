## Introducción
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/17682/` ([link](https://jupiter.challenges.picoctf.org/problem/17682/)) or http://jupiter.challenges.picoctf.org:17682
Never trust the client

## Descripción
Cliente-side : el procesamiento toma lugar en la computadora del usuario, reduce carga, html,js,css
Server-side: el procesamiento es en el servidor, procesamiento dinamico, incrementa carga, php,py,asp.net

La validacion del pass queda del lado del cliente y vemos que la manera de comprobacion es atravez de un arreglo de caracteres 
tomando una subcadena desde la posicion 0 hasta la longitud, haciendolo a cadena a diferentes posiciones.segun el orden en el arreglo.

## Solución 

picoCTF{no_clients_plz_b706c5}