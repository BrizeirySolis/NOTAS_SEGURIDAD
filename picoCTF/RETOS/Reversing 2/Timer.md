## Introducción.
You will find the flag after analysing this apkDownload [here](https://artifacts.picoctf.net/c/449/timer.apk).

1.-Decompile
2.-mobsf or jadx
## Descripción
```
┌──(kali㉿kali)-[~/time]
└─$ sudo apt install jadx    
[sudo] password for kali: 
Installing:                     
  jadx

Summary:
  Upgrading: 0, Installing: 1, Removing: 0, Not Upgrading: 149
  Download size: 104 MB
  Space needed: 115 MB / 53.5 GB available

Get:1 http://kali.download/kali kali-rolling/main amd64 jadx all 1.5.0-0kali2 [104 MB]
Fetched 104 MB in 17s (5,956 kB/s)                                            
Selecting previously unselected package jadx.
(Reading database ... 375737 files and directories currently installed.)
Preparing to unpack .../jadx_1.5.0-0kali2_all.deb ...
Unpacking jadx (1.5.0-0kali2) ...
Setting up jadx (1.5.0-0kali2) ...
Processing triggers for kali-menu (2024.3.1) ...
                                                                               
┌──(kali㉿kali)-[~/time]
└─$ wget -4 https://artifacts.picoctf.net/c/449/timer.apk   
--2024-11-26 01:45:51--  https://artifacts.picoctf.net/c/449/timer.apk
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4678467 (4.5M) [application/octet-stream]
Saving to: ‘timer.apk’

timer.apk           100%[==================>]   4.46M  5.91MB/s    in 0.8s    

2024-11-26 01:45:52 (5.91 MB/s) - ‘timer.apk’ saved [4678467/4678467]

                                                                               
┌──(kali㉿kali)-[~/time]
└─$ sudo mv timer.apk /usr/share/jadx/bin/
                                                                               
┌──(kali㉿kali)-[~/time]
└─$ cd /usr/share/jadx/bin
                                                                               
┌──(kali㉿kali)-[/usr/share/jadx/bin]
└─$ sudo jadx -d out timer.apk && cd out/resources
INFO  - loading ...
INFO  - processing ...
ERROR - finished with errors, count: 3                       
                                                                               
┌──(kali㉿kali)-[/usr/…/jadx/bin/out/resources]
└─$ cat AndroidManifest.xml | grep pico
    android:versionName="picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}"

```
## Solución 
picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}