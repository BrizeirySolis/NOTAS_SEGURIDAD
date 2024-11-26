## Introducción
What does asm3(0xd2c26416,0xe6cf51f0,0xe54409d5) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/df999527eaecf46f259c4337a820856c/test.S)

1.-more(?) [registers](https://wiki.skullsecurity.org/index.php?title=Registers)

## Descripción
```
[ arg1 ]  <--- ebp+0x8  (0xd2c26416)
[ arg2 ]  <--- ebp+0xc  (0xe6cf51f0)
[ arg3 ]  <--- ebp+0x10 (0xe54409d5)
asm3:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   xor    eax,eax
        <+5>:   mov    ah,BYTE PTR [ebp+0x9]
        <+8>:   shl    ax,0x10
        <+12>:  sub    al,BYTE PTR [ebp+0xe]
        <+15>:  add    ah,BYTE PTR [ebp+0xf]
        <+18>:  xor    ax,WORD PTR [ebp+0x12]
        <+22>:  nop
        <+23>:  pop    ebp
        <+24>:  ret  
```
## Solución 
 0x375