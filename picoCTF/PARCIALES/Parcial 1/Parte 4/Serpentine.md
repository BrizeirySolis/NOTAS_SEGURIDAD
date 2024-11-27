## Introducción
Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/37/serpentine.py)
1.-Try running the script and see what happens
2.-In the webshell, try examining the script with a text editor like `nano`
3.-To exit `nano`, press Ctrl and x and follow the on-screen prompts.
4.-The `str_xor` function does not need to be reverse engineered for this challenge.
## Descripción
```
┌──(kali㉿kali)-[~/pw3]
└─$ wget -4 https://artifacts.picoctf.net/c/37/serpentine.py  
--2024-11-27 01:48:07--  https://artifacts.picoctf.net/c/37/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: ‘serpentine.py’

serpentine.py        100%[=====================>]   2.49K  --.-KB/s    in 0s      

2024-11-27 01:48:07 (45.0 MB/s) - ‘serpentine.py’ saved [2550/2550]

                                                                                   
┌──(kali㉿kali)-[~/pw3]
└─$ nano serpentine.py
                                                                                   
┌──(kali㉿kali)-[~/pw3]
└─$ python3 serpentine.py                                
/home/kali/pw3/serpentine.py:38: SyntaxWarning: invalid escape sequence '\ '
  '''

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}
a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) 

```
## Solución 
picoCTF{7h3_r04d_l355_7r4v3l3d_8e47d128}