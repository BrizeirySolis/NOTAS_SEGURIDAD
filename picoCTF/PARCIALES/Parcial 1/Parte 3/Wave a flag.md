## Introducción

1.-This program will only work in the webshell or another Linux computer.
2.-To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm`
3.-Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
4.--h and --help are the most common arguments to give to programs to get more information from them!
5.-Not every program implements help features like -h and --help.
## Descripción
```

┌──(kali㉿kali)-[/]
└─$ wget -4 https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm              
--2024-11-27 00:46:34--  https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
warm: Permission denied

Cannot write to ‘warm’ (Permission denied).
                                                                                   
┌──(kali㉿kali)-[/]
└─$ ls           
bin   home            lib32       mnt   run       sys  vmlinuz
boot  initrd.img      lib64       opt   sbin      tmp  vmlinuz.old
dev   initrd.img.old  lost+found  proc  srv       usr
etc   lib             media       root  swapfile  var
                                                                                   
┌──(kali㉿kali)-[/]
└─$ chmod +x warm
chmod: cannot access 'warm': No such file or directory
                                                                                   
┌──(kali㉿kali)-[/]
└─$ ./warm
zsh: no such file or directory: ./warm
                                                                                   
┌──(kali㉿kali)-[/]
└─$              



┌──(kali㉿kali)-[/]
└─$ cd ~         
                                                                                   
┌──(kali㉿kali)-[~]
└─$ wget -4 https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm
--2024-11-27 00:47:53--  https://mercury.picoctf.net/static/f95b1ee9f29d631d99073e34703a2826/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: ‘warm’

warm                 100%[=====================>]  10.68K  --.-KB/s    in 0s      

2024-11-27 00:47:53 (106 MB/s) - ‘warm’ saved [10936/10936]

                                                                                   
┌──(kali㉿kali)-[~]
└─$ chmls        
Command 'chmls' not found, did you mean:
  command 'cpmls' from deb cpmtools
Try: sudo apt install <deb name>
                                                                                   
┌──(kali㉿kali)-[~]
└─$ ls
asciiftw   keygenme-trial.py    playfair.py          script.py     warm
Desktop    level2.flag.txt.enc  Public               solvebh.py    wget-log
Documents  level2.py            pw1                  solver.py     wget-log.1
doll       message.txt          pw2                  tab
Downloads  nopad.py             ruby-install-0.8.0   Templates
file.py    oc                   ruby-install.tar.gz  unpackme-upx
grep       Pictures             sAN                  Videos
                                                                                   
┌──(kali㉿kali)-[~]
└─$ chmod +x warm
                                                                                   
┌──(kali㉿kali)-[~]
└─$ ./warm
Hello user! Pass me a -h to learn what I can do!
                                                                                   
┌──(kali㉿kali)-[~]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}

```

## Solución 
picoCTF{b1scu1ts_4nd_gr4vy_f0668f62}