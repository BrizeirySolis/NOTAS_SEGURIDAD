## Introducción.
What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/288/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

Download and try to decompile the file.
## Descripción
```
─(kali㉿kali)-[~/s2]
└─$ wget -4 https://artifacts.picoctf.net/c/288/SafeOpener.class
--2024-11-26 01:35:30--  https://artifacts.picoctf.net/c/288/SafeOpener.class
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2036 (2.0K) [application/octet-stream]
Saving to: ‘SafeOpener.class’

SafeOpener.class    100%[==================>]   1.99K  --.-KB/s    in 0s      

2024-11-26 01:35:31 (66.5 MB/s) - ‘SafeOpener.class’ saved [2036/2036]

                                                                               
┌──(kali㉿kali)-[~/s2]
└─$ cat SafeOppener.class         
cat: SafeOppener.class: No such file or directory
                                                                               
┌──(kali㉿kali)-[~/s2]
└─$ cat SafeOpener.class 
����4�
CDE     FG
H
I
JL      FN
OP
Q
RS
.T
OU
VW
X
Y
[
]
R`ab<init>()VCodeLineNumberTableLocalVariableTablethis
                                                      LSafeOpener;main([Ljava/lang/String;)VisOpenZargs[Ljava/lang/Stringkeyboard▒Ljava/io/BufferedReader;encodercEncoder
           InnerClasses▒Ljava/util/Base64$Encoder;
StackMapTable*Dcdang/String;keyiI
ExceptionsopenSafe(Ljava/lang/String;)password
SourceFileSafeOpener.java
                         java/io/BufferedReaderjava/io/InputStreamReaderf
                                                                         gh
                                                                           i
                                                                            jk
                                                                              lm
 noEnter password for the safe: p
                                 qr
                                   std
                                      uv
                                        wx
                                          yr
                                            >?java/lang/StringBuilder
You have  
          z{
            z| attempt(s) left
                              }t,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_5bfbd6f1}
                                                                             ~
                                                                              Sesame openPassword is incorrect

SafeOpenerjava/lang/Object▒java/util/Base64$Encoderjava/lang/Stringjava/io/IOExceptionjava/lang/SysteminLjava/io/InputStream;▒(Ljava/io/InputStream;)V(Ljava/io/Reader;)Vjava/util/Base64
getEncoder()Ljava/util/Base64$Encoder;outLjava/io/PrintStream;java/io/PrintStreamprint(Ljava/lang/String;)readLine()Ljava/lang/StringgetBytes()[BencodeToString([B)Ljava/lang/String;printlnappend-(Ljava/lang/String;)Ljava/lang/StringBuilder;(I)Ljava/lang/StringBuildertoStringequals(Ljava/lang/Object;)Z! /*��!"
                                                                         #$   %& <x�Y�Y���L�:6�T�
�
 +�
�.4>EKPq▒���HK,'�!▒!f+,b-1_23[43 X567� 89:;;�V<=        >? u▒L*+��
                    "#&'"@323�;AB0
.J/                                                                                    
┌──(kali㉿kali)-[~/s2]
└─$ 

```
## Solución 
picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_5bfbd6f1}