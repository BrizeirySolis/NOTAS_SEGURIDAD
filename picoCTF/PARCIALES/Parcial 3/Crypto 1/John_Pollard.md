## Introducción
Sometimes RSA [certificates](https://jupiter.challenges.picoctf.org/static/c882787a19ed5d627eea50f318d87ac5/cert) are breakable
The flag is in the format picoCTF{p,q}
Try swapping p and q if it does not work
## Descripción
1. Decodifique el certificado RSA en https://certlogik.com/decoder/
2. Encuentre el valor del módulo en el certificado decodificado:
		Modulus: 4966306421059967 (0x11a4d45212b17f)
1. Utilice factorizar en p y q: `factor(0x11a4d45212b17f)`
![[Pasted image 20241122140124.png]]
La factorización del número 0x11a4d45212b17f0x11a4d45212b17f (en decimal: 1964964509707519919649645097075199) es:

p=73176001,q=67867967
## Solución 
picoCTF{73176001,67867967}