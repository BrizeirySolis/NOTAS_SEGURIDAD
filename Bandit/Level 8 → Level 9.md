## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos Acceso 
ssh bandit8@bandit.labs.overthewire.org -p 2220
 dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
## Comandos
wc: obtener información estadística sobre un archivo de texto, como el número de líneas, palabras y caracteres y nombre 

sort:  ordena las lineas en forma alfabetica 
uniq -u: busca una linea unica

| :  redirige la salida de un comando al otro 
## Código
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
bandit8@bandit:~$
```

## Solución 
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
## Nota Adicional


