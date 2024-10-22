## Objetivo
There is a git repository at ssh://bandit30-git@localhost/home/bandit30-git/repo. The password for the user bandit30-git is the same as for the user bandit30.

Clone the repository and find the password for the next level.
## Datos Acceso 

Server :ssh bandit30@bandit.labs.overthewire.org -p 2220  
Password :bbc96594b4e001778eee9975372716b2
## Comandos
El comando para ver las etiquetas es . Para crear una etiqueta, el comando es . Para ver más detalles, como el mensaje de etiqueta y la confirmación, puede usar el siguiente comando: .`git tag``git tag -a <tag_name> -m <"tag description/message">``git show <tag_name>`

## Codigo 
```
```bash
bandit30@bandit:~$ mktemp -d
/tmp/tmp.iFnbTcdMf4
bandit30@bandit:~$ cd /tmp/tmp.iFnbTcdMf4
bandit30@bandit:/tmp/tmp.iFnbTcdMf4$ git clone ssh://bandit30-git@localhost/home/bandit30-git/repo
bandit30@bandit:/tmp/tmp.iFnbTcdMf4$ ls
repo
bandit30@bandit:/tmp/tmp.iFnbTcdMf4$ cd repo
bandit30@bandit:/tmp/tmp.iFnbTcdMf4/repo$ ls -la
total 16
drwxr-sr-x 3 bandit30 root 4096 Jul  3 13:05 .
drwx--S--- 3 bandit30 root 4096 Jul  3 13:05 ..
drwxr-sr-x 8 bandit30 root 4096 Jul  3 13:05 .git
-rw-r--r-- 1 bandit30 root   30 Jul  3 13:05 README.md
bandit30@bandit:/tmp/tmp.iFnbTcdMf4/repo$ cat README.md 
just an epmty file... muahaha
```
bandit30@bandit:/tmp/tmp.iFnbTcdMf4/repo$ git show secret
47e603bb428404d265f59c42920d81e5

## Solución
`47e603bb428404d265f59c42920d81e5`