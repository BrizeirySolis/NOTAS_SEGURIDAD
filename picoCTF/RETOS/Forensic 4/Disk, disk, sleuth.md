## Introducción
All we know is the file with the flag is named `down-at-the-bottom.txt`... Disk image: [dds2-alpine.flag.img.gz](https://mercury.picoctf.net/static/6cd5ca45d75250451931cea538fb38c0/dds2-alpine.flag.img.gz)

1.-The sleuthkit has some great tools for this challenge as well.
2.-Sleuthkit docs here are so helpful: [TSK Tool Overview](http
3.-This disk can also be booted with qemu!://wiki.sleuthkit.org/index.php?title=TSK_Tool_Overview)
4.- Using your own computer, you could use qemu to boot from this disk!
## Descripción
```
──(kali㉿kali)-[~/diskSleuth]
└─$ wget -4 https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz
--2024-11-24 23:29:40--  https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: ‘dds1-alpine.flag.img.gz’

dds1-alpine.flag.img. 100%[=========================>]  28.39M  8.46MB/s    in 3.6s    

2024-11-24 23:29:44 (7.78 MB/s) - ‘dds1-alpine.flag.img.gz’ saved [29768910/29768910]

                                                                                        
┌──(kali㉿kali)-[~/diskSleuth]
└─$ srch_strings dds1-alpine.flag.img | grep pico
               
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_564ff1a0}

```
## Comandos
wget -4 https://mercury.picoctf.net/static/920731987787c93839776ce457d5ecd6/dds1-alpine.flag.img.gz

srch_strings dds1-alpine.flag.img | grep pico

## Solución 
 SAY picoCTF{f0r3ns1c4t0r_n30phyt3_564ff1a0}

