## Objetivo
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.  
You do not need to create new connections each time
## Datos Acceso 
Server :  ssh bandit24@bandit.labs.overthewire.org -p 2220
Password : gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
## Comandos

- **`grep`**: Comando para buscar patrones en texto.
- **`-v`**: Opción que invierte la selección, mostrando solo las líneas que no coinciden con el patrón.
## Codigo 
```
bandit24@bandit:~$ ^C
bandit24@bandit:~$ gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8: command not found
bandit24@bandit:~$ for i in {0000..0003}; do echo UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ $i ; done
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0000
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0001
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0002
UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ 0003
bandit24@bandit:~$ for i in {0000..9999}; do echo VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar $i; done | nc localhost 30002 | grep -v
Wrong
Usage: grep [OPTION]... PATTERNS [FILE]...
Try 'grep --help' for more information.
Wrong: command not found
bandit24@bandit:~$
```

## Solución
iCi86ttT4KSNe1armKiwbQNmB3YJP3q4