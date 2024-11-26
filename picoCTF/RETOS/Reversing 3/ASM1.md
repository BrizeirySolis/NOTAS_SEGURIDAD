## Introducción
What does asm1(0x2e0) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/f1c2358ff7d1e9386e41552c549cf2f6/test.S)

1.- assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)
## Descripción
```
asm1:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   cmp    DWORD PTR [ebp+0x8],0x3fb   ; Compare input with 0x3FB (1019)
        <+10>:  jg     0x512 <asm1+37>             ; Jump if greater
        <+12>:  cmp    DWORD PTR [ebp+0x8],0x280   ; Compare input with 0x280 (640)
        <+19>:  jne    0x50a <asm1+29>             ; Jump if not equal
        <+21>:  mov    eax,DWORD PTR [ebp+0x8]     ; Move input to eax
        <+24>:  add    eax,0xa                     ; Add 10 to eax
        <+27>:  jmp    0x529 <asm1+60>             ; Jump to end
        <+29>:  mov    eax,DWORD PTR [ebp+0x8]     ; Move input to eax
        <+32>:  sub    eax,0xa                     ; Subtract 10 from eax
        <+35>:  jmp    0x529 <asm1+60>             ; Jump to end
        <+37>:  cmp    DWORD PTR [ebp+0x8],0x559   ; Compare input with 0x559 (1369)

```

## Solución 
0x2d6