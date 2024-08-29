## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos Acceso 
Server :  ssh bandit11@bandit.labs.overthewire.org -p 2220
Password : dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
## Comandos
 tr [a-zA-Z] [n-za-mN-ZA-M] : decodificacion para rot13
## Codigo 

FORMA 1
```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
bandit11@bandit:~$
```
FORMA 2

```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4
bandit11@bandit:~$ python3
Python 3.12.3 (main, Apr 10 2024, 05:33:47) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import codecs
>>> codecs.decode('Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4','rot13'
)
'The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4'
>>>
```
## Solución
7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4