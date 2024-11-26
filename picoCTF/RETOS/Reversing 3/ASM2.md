## Introducción
What does asm2(0xb,0x2e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/717467c8c8b4332ea5873ad8fe7b2dad/test.S)

1.-assembly [conditions](https://www.tutorialspoint.com/assembly_programming/assembly_conditions.htm)

## Descripción
```
asm2:
        <+0>:   push   ebp                      ; Save the base pointer
        <+1>:   mov    ebp,esp                  ; Set up the stack frame
        <+3>:   sub    esp,0x10                 ; Allocate space for local variables
        <+6>:   mov    eax,DWORD PTR [ebp+0xc]   ; Move the first argument (0xb) into eax
        <+9>:   mov    DWORD PTR [ebp-0x4],eax   ; Store the first argument at [ebp-0x4]
        <+12>:  mov    eax,DWORD PTR [ebp+0x8]   ; Move the second argument (0x2e) into eax
        <+15>:  mov    DWORD PTR [ebp-0x8],eax   ; Store the second argument at [ebp-0x8]
        <+18>:  jmp    0x509 <asm2+28>          ; Jump to the comparison
        <+20>:  add    DWORD PTR [ebp-0x4],0x1   ; Increment the value at [ebp-0x4] by 1
        <+24>:  sub    DWORD PTR [ebp-0x8],0xffffff80 ; Subtract 0x80 (128) from the value at [ebp-0x8]
        <+28>:  cmp    DWORD PTR [ebp-0x8],0x63f3 ; Compare [ebp-0x8] with 0x63F3 (25523 in decimal)
        <+35>:  jle    0x501 <asm2+20>           ; If [ebp-0x8] <= 0x63F3, jump back to <asm2+20>
        <+37>:  mov    eax,DWORD PTR [ebp-0x4]   ; Return the value of [ebp-0x4] in eax
        <+40>:  leave                            ; Clean up the stack frame
        <+41>:  ret                              ; Return the result

```

## Solución 

0xf6
