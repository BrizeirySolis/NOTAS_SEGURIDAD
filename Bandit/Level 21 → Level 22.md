## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

## Datos Acceso 

Server :  ssh bandit21@bandit.labs.overthewire.org -p 2220
Password : EeoULMCra2q0dSkYj561DX7s1CpBuOBt
## Comandos
- `cat`: Es un comando que se utiliza para mostrar el contenido de archivos en la terminal.
    
- `/etc/cron.d/cronjob_bandit22`: Es la ruta al archivo que deseas visualizar. En este caso, el archivo está ubicado en el directorio `/etc/cron.d/`, que es un lugar común para almacenar archivos de configuración de cron jobs en sistemas Unix y Linux.

## Codigo 
```
bandit21@bandit:~$ cat /etc/crontab
# /etc/crontab: system-wide crontab
# Unlike any other crontab you don't have to run the `crontab'
# command to install the new version when you edit this file
# and files in /etc/cron.d. These files also have username fields,
# that none of the other crontabs do.

SHELL=/bin/sh
# You can also override PATH, but by default, newer versions inherit it from the environment
#PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

# Example of job definition:
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# |  |  |  |  |
# *  *  *  *  * user-name command to be executed
17 *    * * *   root    cd / && run-parts --report /etc/cron.hourly
25 6    * * *   root    test -x /usr/sbin/anacron || { cd / && run-parts --report /etc/cron.daily; }
47 6    * * 7   root    test -x /usr/sbin/anacron || { cd / && run-parts --report /etc/cron.weekly; }
52 6    1 * *   root    test -x /usr/sbin/anacron || { cd / && run-parts --report /etc/cron.monthly; }
#
bandit21@bandit:~$ ls -la /etc/cron.d
total 44
drwxr-xr-x   2 root root  4096 Jul 17 15:59 .
drwxr-xr-x 121 root root 12288 Aug  1 14:49 ..
-rw-r--r--   1 root root   120 Jul 17 15:57 cronjob_bandit22
-rw-r--r--   1 root root   122 Jul 17 15:57 cronjob_bandit23
-rw-r--r--   1 root root   120 Jul 17 15:57 cronjob_bandit24
-rw-r--r--   1 root root   201 Apr  8 14:38 e2scrub_all
-rwx------   1 root root    52 Jul 17 15:59 otw-tmp-dir
-rw-r--r--   1 root root   102 Mar 31 00:06 .placeholder
-rw-r--r--   1 root root   396 Jan  9  2024 sysstat
bandit21@bandit:~$ ls /etc/cron.d
cronjob_bandit22  cronjob_bandit24  otw-tmp-dir
cronjob_bandit23  e2scrub_all       sysstat
bandit21@bandit:~$ ls /etc/cron.d^C
bandit21@bandit:~$ cat /etc/cron.d/cronjob_bandit22
@reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
bandit21@bandit:~$ cat /usr/bin/cronjob_bandit22.sh
#!/bin/bash
chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
bandit21@bandit:~$ cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
bandit21@bandit:~$
```
## Solución
tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q