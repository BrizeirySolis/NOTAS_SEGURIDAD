## Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
## Datos Acceso 
ssh bandit4@bandit.labs.overthewire.org -p 2220
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
## Comandos
file ./*:  nos dise que tipo de contenido tiene cada archivo
## Código
```
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```
## Solución 
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
## Nota Adicional
*: significa todos
file : el nombre del archivo y su tipo