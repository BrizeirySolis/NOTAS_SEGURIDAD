## Introducción
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/73/challenge.zip)

1.-In collaborative projects, many users can make many changes. How can you see the changes within one file?
2.- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
3.-You can use `python3 <file>.py` to try running the code, though you won't need to for this challenge.
## Descripción
```
 86  wget -4 https://primer.picoctf.org/#_git_version_control
   87  cd drop-in
   88  ls -la
   89  unzip challenge.zip
   90  ls
   91  cd drop-in
   92  python3 message.py
   93  git init
   94  git log | grep picoCTF
   95  git log | grep picoCTF{

┌──(kali㉿kali)-[~/picobg/drop-in]
┌──(kali㉿kali)-[~/picobg/drop-in]
└─$ git log | grep picoCTF{
Author: picoCTF{@sk_th3_1nt3rn_e9957ce1} <ops@picoctf.com>

```

## Solución 
picoCTF{@sk_th3_1nt3rn_e9957ce1} 