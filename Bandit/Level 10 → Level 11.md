## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos Acceso 
Server :  ssh bandit10@bandit.labs.overthewire.org -p 2220
Password : FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
## Comandos
echo : para imprimir algo
base 64: transforma el texto en base 64
-d: revierte la base64
## Codigo 
```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
bandit10@bandit:~$ echo "hola mundo" | base64
aG9sYSBtdW5kbwo=
bandit10@bandit:~$ echo -n aG9sYSBtdW5kbwo= | base64
YUc5c1lTQnRkVzVrYndvPQ==
bandit10@bandit:~$ echo -n aG9sYSBtdW5kbwo= | base64 -d
hola mundo
bandit10@bandit:~$ base64 -d data.txt
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
bandit10@bandit:~$ cat data.txt | base64 -d
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
bandit10@bandit:~$
```

## Solución
dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr