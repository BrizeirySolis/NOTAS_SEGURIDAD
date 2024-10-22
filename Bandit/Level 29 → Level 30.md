## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos Acceso 

Server :  ssh [bandit29@bandit.labs.overthewire.org](mailto:bandit29@bandit.labs.overthewire.org) -p 2220
Password :
## Comandos

De forma predeterminada, sin argumentos, enumera las confirmaciones realizadas en el repositorio en orden cronológico inverso. Usamos el comando con opción para mostrar el diff introducido en cada commit.`git log``git log``-p`
## Codigo 
```
bandit29@bandit:~$ mkdir -p /tmp/secttp  
bandit29@bandit:~$ cd /tmp/secttp  
bandit29@bandit:/tmp/secttp$ git clone ssh://bandit29-git@localhost/home/bandit29-git/repo  
Cloning into 'repo'...  
Could not create directory '/home/bandit29/.ssh'.  
The authenticity of host 'localhost (127.0.0.1)' can't be established.  
ECDSA key fingerprint is SHA256:98UL0ZWr85496EtCRkKlo20X3OPnyPSB5tB5RPbhczc.  
Are you sure you want to continue connecting (yes/no)? yes  
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).  
This is a OverTheWire game server. More information on [http://www.overthewire.org/wargames](http://www.overthewire.org/wargames)bandit29-git@localhost's password:  
bbc96594b4e001778eee9975372716b2remote: Counting objects: 16, done.  
remote: Compressing objects: 100% (11/11), done.  
remote: Total 16 (delta 2), reused 0 (delta 0)  
Receiving objects: 100% (16/16), done.  
Resolving deltas: 100% (2/2), done.  
bandit29@bandit:/tmp/secttp$ cd repo/  
bandit29@bandit:/tmp/secttp/repo$
```

## Solución
bbc96594b4e001778eee9975372716b2