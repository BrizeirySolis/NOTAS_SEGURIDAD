## Introducción
Download this disk image, find the key and log into the remote machine.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://artifacts.picoctf.net/c/71/disk.img.gz)
- Remote machine: `ssh -i key_file -p 56996 ctf-player@saturn.picoctf.net`

## Descripción
                                                                              
┌──(kali㉿kali)-[~/Operation_Oni]
└─$ mmls disk.img      
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000471039   0000264192   Linux (0x83)
                                                                               
┌──(kali㉿kali)-[~/Operation_Oni]
└─$ fls -o 0000206848 disk.img -r

──(kali㉿kali)-[~/Operation_Oni]
└─$ fls -o 000411648 disk.img 470 -r  
Cannot determine file system type
                                                                               
┌──(kali㉿kali)-[~/Operation_Oni]
└─$ fls -o 0000206848 disk.img 470 -r 
r/r 2344:       .ash_history
d/d 3916:       .ssh
+ r/r 2345:     id_ed25519
+ r/r 2346:     id_ed25519.pub
                                                                               
┌──(kali㉿kali)-[~/Operation_Oni]
└─$ icat -o 0000206848 disk.img 2345   
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW
QyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLAAAAJgxpYKDMaWC
gwAAAAtzc2gtZWQyNTUxOQAAACBgrXe4bKNhOzkCLWOmk4zDMimW9RVZngX51Y8h3BmKLA
AAAECItu0F8DIjWxTp+KeMDvX1lQwYtUvP2SfSVOfMOChxYGCtd7hso2E7OQItY6aTjMMy
KZb1FVmeBfnVjyHcGYosAAAADnJvb3RAbG9jYWxob3N0AQIDBAUGBw==
-----END OPENSSH PRIVATE KEY-----
                                                                               
┌──(kali㉿kali)-[~/Operation_Oni]
└─$ icat -o 0000206848 disk.img 2345 > key_file

┌──(kali㉿kali)-[~/Operation_Oni]
└─$ chmod 600 key_file        
─(kali㉿kali)-[~/Operation_Oni]
└─$ ssh -i key_file -p 56996 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:56996 ([13.59.203.175]:56996)' can't be established.

ctf-player@challenge:~$ cat flag.txt
picoCTF{k3y_5l3u7h_af277f77}ctf-player@challenge:~$ ^C

## Comandos

## Solución 
