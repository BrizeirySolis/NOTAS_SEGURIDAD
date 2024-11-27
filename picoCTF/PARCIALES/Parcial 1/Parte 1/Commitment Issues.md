## Introducción
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/137/challenge.zip)
1.-Version control can help you recover files if you change or lose them!
2.-Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
3.-You can 'checkout' commits to see the files inside them
## Descripción

```
┌──(kali㉿kali)-[~/ci]
└─$ wget -4 https://artifacts.picoctf.net/c_titan/137/challenge.zip
--2024-11-26 21:16:04--  https://artifacts.picoctf.net/c_titan/137/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.61, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19197 (19K) [application/octet-stream]
Saving to: ‘challenge.zip’

challenge.zip        100%[=====================>]  18.75K  --.-KB/s    in 0.01s   

2024-11-26 21:16:05 (1.69 MB/s) - ‘challenge.zip’ saved [19197/19197]

                                                                                   
┌──(kali㉿kali)-[~/ci]
└─$ ls
challenge.zip
                                                                                   
┌──(kali㉿kali)-[~/ci]
└─$ unzip challenge.zip
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/fc/
 extracting: drop-in/.git/objects/fc/a28bbf8dde2f49246166ae6512a1046fc4cbc3  
   creating: drop-in/.git/objects/61/
 extracting: drop-in/.git/objects/61/db7d05a8b7657aedc1e13320ca53623a364fe7  
   creating: drop-in/.git/objects/ea/
 extracting: drop-in/.git/objects/ea/859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0  
   creating: drop-in/.git/objects/d5/
 extracting: drop-in/.git/objects/d5/52d1ecd2d83fa2e65b6724d1ff73b45a7d59b7  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/1ab266b7a3a1cd099bb509f82b7a2d03aecd03  
   creating: drop-in/.git/objects/ef/
 extracting: drop-in/.git/objects/ef/0b7cc6b98367fa168573c931e0f7098ef59182  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
 extracting: drop-in/message.txt     
                                                                                   
┌──(kali㉿kali)-[~/ci]
└─$ ls
challenge.zip  drop-in
                                                                                   
┌──(kali㉿kali)-[~/ci]
└─$ cd drop-in
                                                                                   
┌──(kali㉿kali)-[~/ci/drop-in]
└─$ ls
message.txt
                                                                                   
┌──(kali㉿kali)-[~/ci/drop-in]
└─$ git init                   
Reinitialized existing Git repository in /home/kali/ci/drop-in/.git/
                                                                                   
┌──(kali㉿kali)-[~/ci/drop-in]
└─$ git log                
commit ef0b7cc6b98367fa168573c931e0f7098ef59182 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    remove sensitive info

commit ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:06:20 2024 +0000

    create flag
                                                                                   
┌──(kali㉿kali)-[~/ci/drop-in]
└─$ git checkout ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Note: switching to 'ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ea859bf create flag
                                                                                   
┌──(kali㉿kali)-[~/ci/drop-in]
└─$ cat message.txt               
picoCTF{s@n1t1z3_cf09a485}

```

## Solución 
picoCTF{s@n1t1z3_cf09a485}