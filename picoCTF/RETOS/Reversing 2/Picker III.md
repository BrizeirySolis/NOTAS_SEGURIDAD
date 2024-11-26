## Introducción
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 57005`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/525/picker-III.py).

1.-Is there any way to modify the function table?
## Descripción
```

┌──(kali㉿kali)-[~/p3]
└─$ wget -4 https://artifacts.picoctf.net/c/525/picker-III.py
--2024-11-26 01:26:22--  https://artifacts.picoctf.net/c/525/picker-III.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4439 (4.3K) [application/octet-stream]
Saving to: ‘picker-III.py’

picker-III.py       100%[==================>]   4.33K  --.-KB/s    in 0s      

2024-11-26 01:26:22 (209 MB/s) - ‘picker-III.py’ saved [4439/4439]

                                                                               
┌──(kali㉿kali)-[~/p3]
└─$ nc saturn.picoctf.net 57005
==> 3
Please enter variable name to write: win
Please enter new value of variable: 
                                                                               
┌──(kali㉿kali)-[~/p3]
└─$ nc saturn.picoctf.net 57005
==> 3
Please enter variable name to write: getRandomNumber 
Please enter new value of variable: win
==> ?

This program fixes vulnerabilities in its predecessor by limiting what
functions can be called to a table of predefined functions. This still puts
the user in charge, but prevents them from calling undesirable subroutines.

* Enter 'quit' to quit the program.
* Enter 'help' for this text.
* Enter 'reset' to reset the table.
* Enter '1' to execute the first function in the table.
* Enter '2' to execute the second function in the table.
* Enter '3' to execute the third function in the table.
* Enter '4' to execute the fourth function in the table.

Here's the current table:
  
1: print_table
2: read_variable
3: write_variable
4: getRandomNumber
==> 4
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x37 0x68 0x31 0x35 0x5f 0x31 0x35 0x5f 0x77 0x68 0x34 0x37 0x5f 0x77 0x33 0x5f 0x67 0x33 0x37 0x5f 0x77 0x31 0x37 0x68 0x5f 0x75 0x35 0x33 0x72 0x35 0x5f 0x31 0x6e 0x5f 0x63 0x68 0x34 0x72 0x67 0x33 0x5f 0x61 0x31 0x38 0x36 0x66 0x39 0x61 0x63 0x7d 
==> ^C

```
![[Pasted image 20241126002755.png]]
## Solución 
picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_a186f9ac}