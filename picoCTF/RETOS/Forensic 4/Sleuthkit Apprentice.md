## Introducción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/136/disk.flag.img.gz)

## Descripción

```

┌──(kali㉿kali)-[~/Sleuthkit_App]
└─$ wget -4 https://artifacts.picoctf.net/c/136/disk.flag.img.gz
--2024-11-24 23:39:30--  https://artifacts.picoctf.net/c/136/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.64, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 47534571 (45M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz      100%[=========================>]  45.33M  8.68MB/s    in 5.0s    

2024-11-24 23:39:35 (9.11 MB/s) - ‘disk.flag.img.gz’ saved [47534571/47534571]

                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_App]
└─$ gzip -d disk.flag.img.gz

                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_App]
└─$ mmls disk.flag.img   
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000360447   0000153600   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000360448   0000614399   0000253952   Linux (0x83)
                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_App]
└─$ fls -o 360448 disk.flag.img -r 

┌──(kali㉿kali)-[~/Sleuthkit_App]
└─$ fls -o 360448 disk.flag.img -r 1995
r/r 2363:       .ash_history
d/d 3981:       my_folder
+ r/r * 2082(realloc):  flag.txt
+ r/r 2371:     flag.uni.txt
                                                                                        
┌──(kali㉿kali)-[~/Sleuthkit_App]
└─$ icat -o 360448 disk.flag.img 2371
picoCTF{by73_5urf3r_3497ae6b}

```

## Comandos
shres: borrar archivos de manera segura 

## Solución 
picoCTF{by73_5urf3r_3497ae6b}