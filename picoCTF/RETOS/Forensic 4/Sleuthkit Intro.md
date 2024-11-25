## Introducción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 53133`

## Descripción

```
                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_Intro]
└─$ wget -4 https://artifacts.picoctf.net/c/164/disk.img.gz
--2024-11-24 23:34:24--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: ‘disk.img.gz’

disk.img.gz           100%[=========================>]  28.34M  9.43MB/s    in 3.0s    

2024-11-24 23:34:27 (9.43 MB/s) - ‘disk.img.gz’ saved [29714372/29714372]

                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_Intro]
└─$ mmls disk.img        
Error stat(ing) image file (raw_open: image "disk.img" - No such file or directory)
                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_Intro]
└─$ gzip -d disk.img               
                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_Intro]
└─$ mmls disk.img   
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_Intro]
└─$ nc saturn.picoctf.net 53133
What is the size of the Linux partition in the given disk image?
Length in sectors: 0000202752
0000202752
Great work!
picoCTF{mm15_f7w!}
                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_Intro]
└─$ 

```

## Solución 
picoCTF{mm15_f7w!}