## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos Acceso 
ssh bandit9@bandit.labs.overthewire.org -p 2220
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
## Comandos
strings : xtraer cadenas imprimibles de archivos binarios o de datos con** el comando cadenas de Linux
## Código
```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
\a!;========== the
========== passwordf
========== isc
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
bandit9@bandit:~$
```
## Solución 
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
## Nota Adicional