## Objetivo
The password for the next level is stored in a file called **-** located in the home directory
## Datos Acceso 
ssh bandit1@bandit.labs.overthewire.org -p 2220
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
## Comandos
ls: listar archivos y directorios
cd: cambiar de directorio
cat: crear, fusionar, imprimir y mostrar archivos en Linux. 
file: te permite ver el tipo de archivo con el que estás tratando.
du: para obtener el tamaño total de un directorio y sus archivos en formato legible para el ser humano.
find: Puede usarlo para buscar archivos y directorios en función de varios criterios
## Código
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
bandit1@bandit:~$
```
## Solución 
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
## Nota Adicional
si el  nombre del archivo empieza con - se le pone ./