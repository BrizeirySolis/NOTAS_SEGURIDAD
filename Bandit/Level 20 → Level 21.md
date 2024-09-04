## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos Acceso 

Server :  ssh bandit20@bandit.labs.overthewire.org -p 2220
Password :0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
## Comandos
- `./suconnect`: Este es el nombre de un archivo ejecutable en el directorio actual. El prefijo `./` indica que el archivo se encuentra en el directorio actual y se está ejecutando desde allí.
    
- `2020`: Este es un argumento que se pasa al archivo ejecutable `suconnect`. Sin contexto adicional, es difícil saber qué hace exactamente el argumento `2020`, pero suele representar algún tipo de entrada que el ejecutable necesita para funcionar, como un número de puerto, un identificador, o una opción específica para la ejecución del programa.
## Codigo 
```
bandit20@bandit:~$ nc -lnvp 2020 <<< 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO &
[1] 1701571
bandit20@bandit:~$ Listening on 0.0.0.0 2020

bandit20@bandit:~$ ./suconnect 2020
Connection received on 127.0.0.1 54798
Read: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
Password matches, sending next password
EeoULMCra2q0dSkYj561DX7s1CpBuOBt
[1]+  Done                    nc -lnvp 2020 <<< 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
bandit20@bandit:~$
```
## Solución
 EeoULMCra2q0dSkYj561DX7s1CpBuOBt