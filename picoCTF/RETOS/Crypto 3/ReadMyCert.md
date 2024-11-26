## Introducción
How about we take you on an adventure on exploring certificate signing requestsTake a look at this CSR file [here](https://artifacts.picoctf.net/c/421/readmycert.csr).

1.-Download the certificate signing request and try to read it.
## Descripción
```
┌──(kali㉿kali)-[~/Documentos/crypto/readmycert]
└─$ wget https://artifacts.picoctf.net/c/422/readmycert.csr
--2024-05-16 20:14:30--  https://artifacts.picoctf.net/c/422/readmycert.csr
Resolviendo artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Conectando con artifacts.picoctf.net (artifacts.picoctf.net)[3.161.55.61]:443... conectado.
Petición HTTP enviada, esperando respuesta... 200 OK
Longitud: 997 [application/octet-stream]
Grabando a: «readmycert.csr»

readmycert.csr       100%[====================>]     997  --.-KB/s    en 0s      

2024-05-16 20:14:31 (18.5 MB/s) - «readmycert.csr» guardado [997/997]

                                                                                  
┌──(kali㉿kali)-[~/Documentos/crypto/readmycert]
└─$ file readmycert.csr 
readmycert.csr: PEM certificate request
                                                                                  
┌──(kali㉿kali)-[~/Documentos/crypto/readmycert]
└─$ cat readmycert.csr 

-----BEGIN CERTIFICATE REQUEST-----
MIICpzCCAY8CAQAwPDEmMCQGA1UEAwwdcGljb0NURntyZWFkX215Y2VydF8zYWE4
MDA5MH0xEjAQBgNVBCkMCWN0ZlBsYXllcjCCASIwDQYJKoZIhvcNAQEBBQADggEP
ADCCAQoCggEBAN1PdpW4sKum7AhFubDl86sflki20dWKkZ/iZBYYX/RYqZIWm9ve
pdfwkeiDdz7KriPzM9tTDuJm1kWv8/3AxHrYwliFHK0lsmUYdOcPfrvlh6SIuZwH
vxhrR0DJ0+W5vU+4j9G/hk2+JLMURh8WZadwBhRcfIxk97OXujjvHS9KplMAs5ul
cSSQcv77QkIcxVg1OSDVZoEjTr131g+/Jox3T+uFPEvzF9iq03JMU39oqfGaFL02
EQTaTl8efLIDkGxrKCc+Jhn4e1mD+9UlUmIn9nsOBCYNrnfq4usAL10ZPMDty2Sx
yVTl0171trvCA9DF5PRG6eMYirJOmF18oSUCAwEAAaAmMCQGCSqGSIb3DQEJDjEX
MBUwEwYDVR0lBAwwCgYIKwYBBQUHAwIwDQYJKoZIhvcNAQELBQADggEBAMa7s/l3
mAwJi7LsosPS6/VlZwfTdiJAv+WOKN9T1q2JRHsAGRrW9Gz5p7nSBKJxevRaOMwn
XWK0HqmN3y2/lor50jWzqLhM4TnbKsakXnEIo90XgHoy+n0DL0296Lg/xoXrRgrh
2o3rtZTc+irqUzTRM7Q1F76LNmgtEXqvbOm6Gx2dASPhVAAfylRBCTyz2dYwg2vM
kwt4e5bTvpze/xyTyI8Pydq09YYJe0+a2cHSgcoyGoWXjIK4CUxjBNXAFxSPCcS3
5JRkBnyGo+KL+XtuK9yCX7xBFkwLybK7Mj4TeGiwDsR/0SwqyWGb7Q2m58ay8RVm
pmAIEs21M3236Z4=
-----END CERTIFICATE REQUEST-----

picoCTF{read_mycert_3aa80090}

* Copiamos la llave y la pegamos en la siguiente pagina: https://www.sslshopper.com/csr-decoder.html, abajo nos mostrara la bandera: 
* **CSR Information:**

##### **Common Name:** picoCTF{read_mycert_3aa80090}

##### **Key Size:** 2048 bit
```
## Solución 
picoCTF{read_mycert_3aa80090}