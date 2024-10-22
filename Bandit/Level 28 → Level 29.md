## Objetivo
Hay un repositorio git en via el puerto . La contraseña del usuario es la misma que la del usuario .`ssh://bandit28-git@localhost/home/bandit28-git/repo``2220``bandit28-git``bandit28`

Clona el repositorio y encuentra la contraseña para el siguiente nivel.
## Datos Acceso 

Server
bandit28@bandit.labs.overthewire.org -p 2220`

Password: `0ef186ac70e04ea33b4c1853d2526fa2`
## Comandos

- `git log`, shows us the commit log.
- `git show <commit>`, shows us the content of a commit _(When creating a public repository it is important to be aware of the information you push to it since changes and previous versions are saved. So sensitive data, like passwords, could still be retrieved)._
## Codigo 
```
bash
bandit28@bandit:/tmp/tmp.lGUWKxK6CU/repo$ git show edd935d60906b33f0619605abd1689808ccdd5ee
commit edd935d60906b33f0619605abd1689808ccdd5ee
Author: Morla Porla <morla@overthewire.org>
Date:   Thu May 7 20:14:49 2020 +0200

    fix info leak

diff --git a/README.md b/README.md
index 3f7cee8..5c6457b 100644
--- a/README.md
+++ b/README.md
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.
 ## credentials
 
 - username: bandit29
-- password: bbc96594b4e001778eee9975372716b2
+- password: xxxxxxxxxx
```


## Solución