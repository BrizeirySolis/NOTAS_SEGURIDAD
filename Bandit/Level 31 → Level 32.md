## Objetivo
There is a git repository at ssh://bandit31-git@localhost/home/bandit31-git/repo. The password for the user bandit31-git is the same as for the user bandit31.

Clone the repository and find the password for the next level.
## Datos Acceso 

Server :  ssh bandit31@bandit.labs.overthewire.org -p 2220
Password :  `47e603bb428404d265f59c42920d81e5`
## Comandos


## Codigo 
```
|   |   |
|---|---|
|```<br>1<br> 2<br> 3<br> 4<br> 5<br> 6<br> 7<br> 8<br> 9<br>10<br>11<br>12<br>13<br>14<br>15<br>16<br>17<br>18<br>19<br>20<br>21<br>22<br>```|```bash<br>bandit31@bandit:/tmp/tmp.IhtWdYHfZb/repo$ git add -f key.txt<br>bandit31@bandit:/tmp/tmp.IhtWdYHfZb/repo$ git commit -a<br>Unable to create directory /home/bandit31/.nano: Permission denied<br>It is required for saving/loading search history or cursor positions.<br><br>Press Enter to continue<br><br>[master 35298de] Key file<br> 1 file changed, 1 insertion(+)<br> create mode 100644 key.txt<br>bandit31@bandit:/tmp/tmp.IhtWdYHfZb/repo$ git push -u origin master<br>...<br>remote: ### Attempting to validate files... ####<br>remote: <br>remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.<br>remote: <br>remote: Well done! Here is the password for the next level:<br>remote: 56a9bf19c63d650ce78e6ec0354ee45e<br>remote: <br>remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.<br>remote: <br>...<br>```|
```

## Solución

56a9bf19c63d650ce78e6ec0354ee45e
