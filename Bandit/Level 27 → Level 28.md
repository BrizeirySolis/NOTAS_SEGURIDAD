## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.
## Datos Acceso 
Server :  ssh bandit27@bandit.labs.overthewire.org -p 2220
Password : upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
## Comandos

- **`mktemp`**:
    
    - `mktemp` es una utilidad de línea de comandos que se utiliza para crear archivos o directorios temporales con nombres únicos para evitar colisiones con archivos o directorios existentes.
- **`-d`**:
    
    - La opción `-d` indica que se debe crear un directorio en lugar de un archivo. Si no se proporciona la opción `-d`, `mktemp` creará un archivo temporal en lugar de un directorio.
## Codigo 
```
bandit27@bandit:~$ mktemp -d
/tmp/tmp.RH39ki24pd
bandit27@bandit:~$ cd /tmp/tmp.RH39ki24pd
bandit27@bandit:/tmp/tmp.RH39ki24pd$ git clone ssh://bandit27-
git@localhost:2220/home/bandit27-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)'
can't be established.
ED25519 key fingerprint is
SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting
(yes/no/[fingerprint])? yes
Could not create directory '/home/bandit27/.ssh' (Permission
denied).
Failed to add the host to the list of known hosts
(/home/bandit27/.ssh/known_hosts).

_ _ _ _
| |__ __ _ _ __ __| (_) |_
| '_ \ / _` | '_ \ / _` | | __|
| |_) | (_| | | | | (_| | | |_
|_.__/ \__,_|_| |_|\__,_|_|\__|

This is an OverTheWire game server.
bandit27-git@localhost's password: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
bandit27@bandit:/tmp/tmp.RH39ki24pd$ ls -la
total 76
drwx------ 3 bandit27 bandit27 4096 Feb 23 22:56 .
drwxrwx-wt 1742 root root 69632 Feb 23 22:57 ..
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 23 22:57 repo
bandit27@bandit:/tmp/tmp.RH39ki24pd$ cd repo/
bandit27@bandit:/tmp/tmp.RH39ki24pd/repo$ ls
README
bandit27@bandit:/tmp/tmp.RH39ki24pd/repo$ cat README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19n
```

## Solución
AVanL161y9rsbcJIsFHuw35rjaOM19n