## Introducción
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/ff2585f7afd21b81f69d2fbe37c081ae/VaultDoor1.java)

1.-Look up the charAt() method online.
## Descripción
```
┌──(kali㉿kali)-[~/val1]
└─$ nano bandera
                                                                               
┌──(kali㉿kali)-[~/val1]
└─$ cat bandera | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n" 
d35cr4mbl3_tH3_cH4r4cT3r5_75092e;32                                                                               
┌──(kali㉿kali)-[~/val1]
└─$ java VaultDoor1.java                                           
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Enter vault password: picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_75092e}
Access granted.

```
## Solución 
 picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_75092e}
