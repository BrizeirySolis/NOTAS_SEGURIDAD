## Introducción
Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 30048`.

What can you do with a different pair of ciphertext and plaintext? What if it is not so different after all...
## Descripción
![[Pasted image 20241122173411.png]]
## Comandos
python3 nopad.py

```
from pwn import *
import binascii
r=remote("mercury.picoctf.net",30048)
print(r.recvuntil("n:"))
n=int(r.recvline())
print(n)
print(r.recvuntil("e:"))
e=int(r.recvline())
print(e)
print(r.recvuntil("ciphertext:"))
c=int(r.recvline())
print(c)
print(r.recvuntil("to decrypt:"))
# We will send c*2^e. It decrypts to c^d*2^(ed) = 2*c^d
# It is different, and will decrypt to plaintext*2
r.sendline(str(pow(2,e,n)*c))
print(r.recvuntil("you go:"))
p2=int(r.recvline())
print(p2)
print(p2//2)
st="{:x}".format(p2//2)
print(binascii.unhexlify(st))

```
## Solución 
picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_5052620}