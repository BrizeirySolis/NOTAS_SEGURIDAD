## Introducción
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)
Bits are expensive, I used only a little bit over 100 to save money

## Descripción
http://www.factordb.com/index.php?query=1422450808944701344261903748621562998784243662042303391362692043823716783771691667

```
┌──(kali㉿kali)-[~/mind]
└─$ cat values     
Decrypt my super sick RSA:
c: 843044897663847841476319711639772861390329326681532977209935413827620909782846667
n: 1422450808944701344261903748621562998784243662042303391362692043823716783771691667
e: 65537  


zsh: corrupt history file /home/kali/.zsh_history
┌──(kali㉿kali)-[~/mind]
└─$ python3         
Python 3.12.7 (main, Nov  8 2024, 17:55:36) [GCC 14.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> c=843044897663847841476319711639772861390329326681532977209935413827620909782846667
>>> e=65537
>>> p= 2159947535959146091116171018558446546179
>>> q=658558036833541874645521278345168572231473
>>> n=p*q
>>> n
1422450808944701344261903748621562998784243662042303391362692043823716783771691667
>>> tn=(p-1)*(q-1)
>>> d=pow(e,-1,tn)
>>> m=pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_00264570}'
>>> 
```
## Solución 
picoCTF{sma11_N_n0_g0od_00264570}