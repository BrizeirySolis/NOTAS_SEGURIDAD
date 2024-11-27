## Introducción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/176/challenge.zip)

1.- `git branch -a` will let you see available branches
2.- How can file 'diffs' be brought to the main branch? Don't forget to `git config`!
3.-Merge conflicts can be tricky! Try a text editor like nano, emacs, or vim.
## Descripción
```
┌──(kali㉿kali)-[~/cd]
└─$ cd drop-in                                                     
                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ git init               
Reinitialized existing Git repository in /home/kali/cd/drop-in/.git/
                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ git branch -a
  feature/part-1
  feature/part-2
  feature/part-3
* main
                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ git checkout feature/part-1                     
Switched to branch 'feature/part-1'

┌──(kali㉿kali)-[~/cd/drop-in]
└─$ python flag.py
Printing the flag...
picoCTF{t3@mw0rk_                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ git checkout feature/part-2
Switched to branch 'feature/part-2'
                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ git checkout feature/part-2
Already on 'feature/part-2'
                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ python flag.py             
Printing the flag...
m@k3s_th3_dr3@m_                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ git checkout feature/part-3                                    
Switched to branch 'feature/part-3'
                                                                                   
┌──(kali㉿kali)-[~/cd/drop-in]
└─$ python flag.py             
Printing the flag...
w0rk_2c91ca76}

```

## Solución 
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}