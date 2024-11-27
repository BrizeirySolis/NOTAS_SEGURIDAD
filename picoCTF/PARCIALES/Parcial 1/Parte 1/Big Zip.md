## Introducción
Unzip this archive and find the flag.

- [Download zip file](https://artifacts.picoctf.net/c/503/big-zip-files.zip)
1.- Can grep be instructed to look at every file in a directory and its subdirectories?
## Descripción
```
┌──(kali㉿kali)-[~/bz]
└─$ grep -r "picoCTF"      
big-zip-files/folder_pmbymkjcya/folder_cawigcwvgv/folder_ltdayfmktr/folder_fnpfclfyee/whzxrpivpqld.txt:information on the record will last a billion years. Genes and brains and books encode picoCTF{gr3p_15_m4g1c_ef8790dc}

```
## Solución 
 picoCTF{gr3p_15_m4g1c_ef8790dc}