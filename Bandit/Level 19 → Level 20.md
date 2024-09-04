## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
## Datos Acceso 

Server :  ssh bandit19@bandit.labs.overthewire.org -p 2220
Password : cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
## Comandos
- `./bandit20-do`: Esto parece ser un archivo ejecutable en el directorio actual. El prefijo `./` indica que el archivo se encuentra en el directorio actual y se está ejecutando como un comando.
    
- `cat /etc/bandit_pass/bandit20`: Este es el argumento que se pasa al archivo ejecutable `bandit20-do`. El comando `cat` se utiliza para mostrar el contenido del archivo especificado, en este caso, `/etc/bandit_pass/bandit20`.

## Codigo 
```
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
bandit19@bandit:~$ ./bandit20-do ls /etc/bandit_pass
bandit0   bandit13  bandit18  bandit22  bandit27  bandit31  bandit6
bandit1   bandit14  bandit19  bandit23  bandit28  bandit32  bandit7
bandit10  bandit15  bandit2   bandit24  bandit29  bandit33  bandit8
bandit11  bandit16  bandit20  bandit25  bandit3   bandit4   bandit9
bandit12  bandit17  bandit21  bandit26  bandit30  bandit5
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
```

## Solución
0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO