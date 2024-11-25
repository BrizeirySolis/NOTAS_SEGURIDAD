## Introducción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/212/disk.flag.img.gz)

## Descripción

```
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ wget -4 https://artifacts.picoctf.net/c/212/disk.flag.img.gz
--2024-11-24 23:58:16--  https://artifacts.picoctf.net/c/212/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.64, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 44360923 (42M) [application/octet-stream]
Saving to: ‘disk.flag.img.gz’

disk.flag.img.gz    100%[==================>]  42.31M  8.79MB/s    in 4.7s    

2024-11-24 23:58:22 (8.99 MB/s) - ‘disk.flag.img.gz’ saved [44360923/44360923]

                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ gzip -d disk.flag.img.gz                        

                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ mmls disk.flag.img    
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ fls -o 000411648 disk.flag.img 472                          
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ icat -o 000411648 disk.flag.img 1782 > flag.txt.enc
                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ icat -o 0000411648 disk.flag.img 1875                     
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ openssl aes256 -salt -d in flag.txt.enc -out flag.txt -k unbreakablepassword1234567 

aes256: Extra option: "in"
aes256: Use -help for summary.
                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ cat flag.txt                  
cat: flag.txt: No such file or directory
                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ openssl aes256 -salt -d -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567 

*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
406739D3717F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:
                                                                               
┌──(kali㉿kali)-[~/Operation_Orchid]
└─$ cat flag.txt 
picoCTF{h4un71ng_p457_0a710765}  
```

## Solución 
picoCTF{h4un71ng_p457_0a710765}