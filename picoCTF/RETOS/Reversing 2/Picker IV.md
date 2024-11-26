## Introducción.
Can you figure out how this program works to get the flag?Connect to the program with netcat:`$ nc saturn.picoctf.net 50852`The program's source code can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV.c). The binary can be downloaded [here](https://artifacts.picoctf.net/c/529/picker-IV).

## Descripción
```



┌──(kali㉿kali)-[~/p4]
└─$ wget -4 https://artifacts.picoctf.net/c/529/picker-IV.c 
--2024-11-26 01:31:11--  https://artifacts.picoctf.net/c/529/picker-IV.c
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 839 [application/octet-stream]
Saving to: ‘picker-IV.c’

picker-IV.c         100%[==================>]     839  --.-KB/s    in 0s      

2024-11-26 01:31:12 (16.7 MB/s) - ‘picker-IV.c’ saved [839/839]

                                                                               
┌──(kali㉿kali)-[~/p4]
└─$ wget -4 https://artifacts.picoctf.net/c/529/picker-IV  
--2024-11-26 01:31:23--  https://artifacts.picoctf.net/c/529/picker-IV
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17272 (17K) [application/octet-stream]
Saving to: ‘picker-IV’

picker-IV           100%[==================>]  16.87K  --.-KB/s    in 0.05s   

2024-11-26 01:31:23 (353 KB/s) - ‘picker-IV’ saved [17272/17272]

                                                                               
┌──(kali㉿kali)-[~/p4]
└─$  gdb picker-IV 
GNU gdb (Debian 15.2-1) 15.2
Copyright (C) 2024 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<https://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from picker-IV...
(No debugging symbols found in picker-IV)
(gdb) info function
All defined functions:

Non-debugging symbols:
0x0000000000401000  _init
0x00000000004010e0  putchar@plt
0x00000000004010f0  puts@plt
0x0000000000401100  fclose@plt
0x0000000000401110  printf@plt
0x0000000000401120  fgetc@plt
0x0000000000401130  signal@plt
0x0000000000401140  setvbuf@plt
0x0000000000401150  fopen@plt
0x0000000000401160  __isoc99_scanf@plt
0x0000000000401170  exit@plt
0x0000000000401180  sleep@plt
0x0000000000401190  _start
0x00000000004011c0  _dl_relocate_static_pie
0x00000000004011d0  deregister_tm_clones
0x0000000000401200  register_tm_clones
0x0000000000401240  __do_global_dtors_aux
0x0000000000401270  frame_dummy
0x0000000000401276  print_segf_message
0x000000000040129e  win
0x0000000000401334  main
0x00000000004013d0  __libc_csu_init
0x0000000000401440  __libc_csu_fini
0x0000000000401448  _fini
(gdb) exit
                                                                               
┌──(kali㉿kali)-[~/p4]
└─$ nc saturn.picoctf.net 50852
Enter the address in hex to jump to, excluding '0x': 0x000000000040129e
You input 0x40129e
You won!
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}

```
## Solución 
picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_b8de1af4}