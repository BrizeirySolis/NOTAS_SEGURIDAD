## Introducción
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

1.-Try using a tool like Wireshark.
2.-How can you decrypt the TLS stream?
## Descripción
```

┌──(kali㉿kali)-[~/net1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
--2024-11-25 23:02:22--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap        100%[==================>]  90.36K  --.-KB/s    in 0.09s   

2024-11-25 23:02:23 (999 KB/s) - ‘capture.pcap’ saved [92525/92525]

                                                                               
┌──(kali㉿kali)-[~/net1]
└─$ wgethttps://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key 
zsh: no such file or directory: wgethttps://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
                                                                               
┌──(kali㉿kali)-[~/net1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
--2024-11-25 23:02:55--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key        100%[==================>]   1.66K  --.-KB/s    in 0s      

2024-11-25 23:02:55 (41.1 MB/s) - ‘picopico.key’ saved [1704/1704]

                                                                               
┌──(kali㉿kali)-[~/net1]
└─$ wireshark capture.pcap &
[1] 224681
                                                                               
┌──(kali㉿kali)-[~/net1]
└─$  ** (wireshark:224681) 23:03:51.639555 [WSUtil WARNING] ./wsutil/filter_files.c:242 -- read_filter_list(): '/usr/share/wireshark/cfilters' line 1 doesn't have a quoted filter name.
 ** (wireshark:224681) 23:03:51.640018 [WSUtil WARNING] ./wsutil/filter_files.c:242 -- read_filter_list(): '/usr/share/wireshark/cfilters' line 2 doesn't have a quoted filter name.


┌──(kali㉿kali)-[~/net1]
└─$ strings vulture.jpg -n15
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz

```
## Solución 
picoCTF{honey.roasted.peanuts}
