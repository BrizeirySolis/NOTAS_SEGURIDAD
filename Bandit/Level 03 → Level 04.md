## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos Acceso 
ssh bandit3@bandit.labs.overthewire.org -p 2220
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
## Comandos
ls -la : listar archivos en formato largo y ocultos
## Código
```
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Jul 17 15:57 .
drwxr-xr-x 3 root    root    4096 Jul 17 15:57 ..
-rw-r----- 1 bandit4 bandit3   33 Jul 17 15:57 ...Hiding-From-You
bandit3@bandit:~/inhere$ cat .hidden
cat: .hidden: No such file or directory
bandit3@bandit:~/inhere$ cat .hiding-From-You
cat: .hiding-From-You: No such file or directory
bandit3@bandit:~/inhere$ cat .hidden
cat: .hidden: No such file or directory
bandit3@bandit:~/inhere$ cat ...hiding-From-You
cat: ...hiding-From-You: No such file or directory
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ cls
Command 'cls' not found, but there are 20 similar ones.
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
bandit3@bandit:~/inhere$
```

## Solución 
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
## Nota Adicional
 introduce lo primero del nombre de archivo con tab y se completa
 
