## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos Acceso 
ssh bandit7@bandit.labs.overthewire.org -p 2220
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
## Comandos
wc: obtener información estadística sobre un archivo de texto, como el número de líneas, palabras y caracteres y nombre 

grep: permite filtrar las lineas de un archivo en base a un patron o cadena 

grep -n: muestra la linea en la que enconyro el patron 

wc -l: cuenta las lineas qurtiene 
## Código
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$  wc data.txt
  98567  197133 4184396 data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
bandit7@bandit:~$
```
## Solución 
 dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
## Nota Adicional
grep millionth data.txt : la plabra antes del nombre ayuda a imprimir esa linea 

en el cat | gep hace lo mismo