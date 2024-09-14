## Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos Acceso 
Server :  ssh bandit26@bandit.labs.overthewire.org -p 2220
Password :s0773xxkk0MXfdqOfPRVr9L3jJBUOgCZ
## Comandos
- **`gid`**:
    
    - `gid` significa "Group ID" (Identificador de Grupo). En sistemas Unix/Linux, cada grupo tiene un identificador único (ID) que es un número entero.
- **`11026`**:
    
    - Este es el valor numérico del Group ID (GID). Es el identificador único asignado al grupo al que pertenece el usuario.
- **`(bandit26)`**:
    
    - Esto indica el nombre del grupo asociado con el GID. En este caso, el nombre del grupo es `bandit26`.

## Codigo 
```
bandit26@bandit:~$ bandit26@bandit:~$ ls
bandit27-do text.txt
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
bandit26@bandit:~$ exit
```

## Solución
upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB