## Introducción
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)

## Descripción
```
┌──(kali㉿kali)-[~/ffd]
└─$ wget -4 https://artifacts.picoctf.net/c/501/files.zip   
--2024-11-26 21:20:50--  https://artifacts.picoctf.net/c/501/files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.26, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3995553 (3.8M) [application/octet-stream]
Saving to: ‘files.zip’

files.zip            100%[=====================>]   3.81M  11.8MB/s    in 0.3s    

2024-11-26 21:20:51 (11.8 MB/s) - ‘files.zip’ saved [3995553/3995553]

                                                                                   
┌──(kali㉿kali)-[~/ffd]
└─$ unzip files.zip
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
                                                                                   
┌──(kali㉿kali)-[~/ffd]
└─$ find ./ -name 'uber-secret.txt'
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
                                                                                   
┌──(kali㉿kali)-[~/ffd]
└─$  cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}

```

## Solución 
picoCTF{f1nd_15_f457_ab443fd1}