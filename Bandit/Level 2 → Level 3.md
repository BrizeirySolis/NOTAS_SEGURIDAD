## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos Acceso 
ssh bandit2@bandit.labs.overthewire.org -p 2220
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
## Comandos
   ```
   cat spaces\ in\ this\ filename

```
## Código
  ```
  bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat spaces\in\this\filename
cat: spacesinthisfilename: No such file or directory
bandit2@bandit:~$ cat spaces\ in\ this\ filename
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
bandit2@bandit:~$
```
## Solución 
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
## Nota Adicional
si el nombre del archivo tiene espacios se le pone un  /