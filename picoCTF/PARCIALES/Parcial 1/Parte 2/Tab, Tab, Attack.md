## Introducción
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip)

1.-After `unzip`ing, this problem can be solved with 11 button-presses...(mostly Tab)...
## Descripción
```
┌──(kali㉿kali)-[~/tab]
└─$ wget -4 https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip
--2024-11-26 23:44:51--  https://mercury.picoctf.net/static/9689f2b453ad5daeb73ca7534e4d1521/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4519 (4.4K) [application/octet-stream]
Saving to: ‘Addadshashanammu.zip’

Addadshashanammu.zip 100%[=====================>]   4.41K  --.-KB/s    in 0s      

2024-11-26 23:44:52 (67.7 MB/s) - ‘Addadshashanammu.zip’ saved [4519/4519]

                                                                                   
┌──(kali㉿kali)-[~/tab]
┌──(kali㉿kali)-[~/tab]
└─$ ls
Addadshashanammu.zip
                                                                                   
┌──(kali㉿kali)-[~/tab]
└─$ unzip Addadshashanammu.zip

Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
                                                                                   
┌──(kali㉿kali)-[~/tab]
└─$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
cd: not a directory: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
                                                                                   
┌──(kali㉿kali)-[~/tab]
└─$ cd Addadshashanammu
                                                                                   
┌──(kali㉿kali)-[~/tab/Addadshashanammu]
└─$ ls
Almurbalarammi
                                                                                   
┌──(kali㉿kali)-[~/tab/Addadshashanammu]
└─$ cd Addadshashanammu/Almurbalarammi
cd: no such file or directory: Addadshashanammu/Almurbalarammi
                                                                                   
┌──(kali㉿kali)-[~/tab/Addadshashanammu]
└─$ cd Almurbalarammi  
                                                                                   
┌──(kali㉿kali)-[~/tab/Addadshashanammu/Almurbalarammi]
└─$ ls
Ashalmimilkala
                                                                                   
┌──(kali㉿kali)-[~/tab/Addadshashanammu/Almurbalarammi]
└─$ cd Ashalmimilkala  
                                                                                   
┌──(kali㉿kali)-[~/tab/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└─$ cd Assurnabitashpi  
                                                                                   
┌──(kali㉿kali)-[~/…/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]                                                                                  
└─$ ls
Maelkashishi
                                                                                   
┌──(kali㉿kali)-[~/…/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]                                                                                  
└─$ cd Maelkashishi  
                                                                                   
┌──(kali㉿kali)-[~/…/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└─$ ls
Onnissiralis
                                                                                   
┌──(kali㉿kali)-[~/…/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└─$ cd Onnissiralis  
                                                                                   
┌──(kali㉿kali)-[~/…/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└─$ ls
Ularradallaku
                                                                                   
┌──(kali㉿kali)-[~/…/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└─$ cd Ularradallaku  
                                                                                   
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls
fang-of-haynekhtnamet
                                                                                   
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls              
                                                                                   
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ cd fang-of-haynekhtnamet
cd: not a directory: fang-of-haynekhtnamet
                                                                                   
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}

```
## Solución 
picoCTF{l3v3l_up!_t4k3_4_r35t!_2bcfb2ab}