## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos Acceso 
Server :  ssh bandit12@bandit.labs.overthewire.org -p 2220
Password : 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
## Comandos
xdd: toma datos de la entrada o archivo estándar y proporciona una salida hexadecimal
-r: reverse operation: convert (or patch) hexdump into binary.

file:se utiliza para determinar el tipo de contenido de un archivo.
si s ele agrega - : indica que el comando debe leer la entrada desde la entrada estándar (stdin), en lugar de un archivo específico.

zcat: desempaquetar y mostrar el contenido de archivos comprimidos con el formato `gzip` 

bzcat: para desempaquetar y mostrar el contenido de archivos comprimidos con el formato `bzip2` 

tar: se utiliza para manipular archivos en formato de archivo tar (tape archive)

:`x` se usa para extraer el contenido de un archivo tar, y la :
`O` (mayúscula) se usa para enviar el contenido extraído a la salida estándar (stdout), en lugar de extraerlo a un directorio.
## Codigo 
```
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
## Solución
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

## Notas Adicionales

 Algunos tipos de compresion en Linux
-----------------------------------------------------
 ext comp desc ver en consola
-----------------------------------------------------
.gz gzip gzip -d (gunzip) zcat
.bz2 bzip2 bzip2 -d (bunzip2) bzcat
 .tar tar tar xf tar xO
----------------------------------------------------

otros (instalar) :
.zip zip unzip (7z x)
.rar rar unrar (7z x)