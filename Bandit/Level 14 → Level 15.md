## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos Acceso 
Server :  ssh bandit14@bandit.labs.overthewire.org -p 2220
Password : MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
## Comandos
- **`nc`**: Llama a la herramienta Netcat.
- **`localhost`**: Especifica la dirección del host al que te estás conectando. En este caso, `localhost` se refiere a la máquina local.
- **`30000`**: Especifica el puerto al que deseas conectarte en el host especificado.
## Codigo 
```
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```
## Solución
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo