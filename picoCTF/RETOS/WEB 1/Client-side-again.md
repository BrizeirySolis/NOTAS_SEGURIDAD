## Introducción.
Can you break into this super secure portal? `https://jupiter.challenges.picoctf.org/problem/60786/` ([link](https://jupiter.challenges.picoctf.org/problem/60786/)) or http://jupiter.challenges.picoctf.org:60786
What is obfuscation?
## Descripción
Ofuscación: transformaciones en el coddigo que cambia el codigo expuesto a una versión protegida , casi imposible de entender y evita el reversing. 

primero copeamos la parte de código y la metemos a http://jsnice.org/ para hacerlo un poco mas visible y como vemos que sigue siendo la misma lógica del Clien-side pasado lo que hacemos es combinar posiciones para encontrar la bandera que sea mas legible 

var _0x5a46 = ["f49bf}", "_again_e", "this", "Password Verified", "Incorrect password", "getElementById", "value", "substring", "picoCTF{", "not_this"];


![[Pasted image 20241122131245.png]]

_0x5a46[8]+_0x5a46[9]+_0x5a46[1]+_0x5a46[0]
## Solución 

picoCTF{not_this_again_ef49bf}