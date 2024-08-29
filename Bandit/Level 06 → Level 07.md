## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Datos Acceso 
ssh bandit6@bandit.labs.overthewire.org -p 2220
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
## Comandos
find: buscar segun las caracteristicas requeridas
## Código
```
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x  2 root root 4096 Jul 17 15:56 .
drwxr-xr-x 70 root root 4096 Jul 17 15:58 ..
-rw-r--r--  1 root root  220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root root 3771 Mar 31 08:41 .bashrc
-rw-r--r--  1 root root  807 Mar 31 08:41 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
bandit6@bandit:~$
```
## Solución 
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
## Nota Adicional
-group: grupo 
2:significa eror y lo enviamos a ">/dev/null" el nulo es decir s eocultan los usuarios