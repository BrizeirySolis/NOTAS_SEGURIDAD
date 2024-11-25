## Introducción
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!

1.-There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
2.- Try to think about how the website verifies your login.
## Descripción
* Entramos a la página del reto y en el apartado del menu seleccionamos "Admin Login".
** En el user name ponemos ' or 1=1; que es un sql injection y en password el que sea.

## Solución
picoCTF{s0m3_SQL_f8adf3fb}...
