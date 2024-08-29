## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL/TLS encryption.

Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.
## Datos Acceso 
Server :  ssh bandit15@bandit.labs.overthewire.org -p 2220
Password : 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
## Comandos

- **`openssl`**: Llama a la herramienta OpenSSL.
- **`s_client`**: Especifica que se está utilizando la función de cliente SSL/TLS para establecer una conexión segura.
- **`-connect localhost:30001`**: Indica la dirección y el puerto del servidor al que se desea conectar. En este caso, se está intentando conectar a `localhost` en el puerto `30001`.
## Codigo 
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
---
Certificate chain
 0 s:CN = SnakeOil
   i:CN = SnakeOil
   a:PKEY: rsaEncryption, 4096 (bit); sigalg: RSA-SHA256
   v:NotBefore: Jun 10 03:59:50 2024 GMT; NotAfter: Jun  8 03:59:50 2034 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFBzCCAu+gAwIBAgIUBLz7DBxA0IfojaL/WaJzE6Sbz7cwDQYJKoZIhvcNAQEL
BQAwEzERMA8GA1UEAwwIU25ha2VPaWwwHhcNMjQwNjEwMDM1OTUwWhcNMzQwNjA4
MDM1OTUwWjATMREwDwYDVQQDDAhTbmFrZU9pbDCCAiIwDQYJKoZIhvcNAQEBBQAD
ggIPADCCAgoCggIBANI+P5QXm9Bj21FIPsQqbqZRb5XmSZZJYaam7EIJ16Fxedf+
jXAv4d/FVqiEM4BuSNsNMeBMx2Gq0lAfN33h+RMTjRoMb8yBsZsC063MLfXCk4p+
09gtGP7BS6Iy5XdmfY/fPHvA3JDEScdlDDmd6Lsbdwhv93Q8M6POVO9sv4HuS4t/
jEjr+NhE+Bjr/wDbyg7GL71BP1WPZpQnRE4OzoSrt5+bZVLvODWUFwinB0fLaGRk
GmI0r5EUOUd7HpYyoIQbiNlePGfPpHRKnmdXTTEZEoxeWWAaM1VhPGqfrB/Pnca+
vAJX7iBOb3kHinmfVOScsG/YAUR94wSELeY+UlEWJaELVUntrJ5HeRDiTChiVQ++
wnnjNbepaW6shopybUF3XXfhIb4NvwLWpvoKFXVtcVjlOujF0snVvpE+MRT0wacy
tHtjZs7Ao7GYxDz6H8AdBLKJW67uQon37a4MI260ADFMS+2vEAbNSFP+f6ii5mrB
18cY64ZaF6oU8bjGK7BArDx56bRc3WFyuBIGWAFHEuB948BcshXY7baf5jjzPmgz
mq1zdRthQB31MOM2ii6vuTkheAvKfFf+llH4M9SnES4NSF2hj9NnHga9V08wfhYc
x0W6qu+S8HUdVF+V23yTvUNgz4Q+UoGs4sHSDEsIBFqNvInnpUmtNgcR2L5PAgMB
AAGjUzBRMB0GA1UdDgQWBBTPo8kfze4P9EgxNuyk7+xDGFtAYzAfBgNVHSMEGDAW
gBTPo8kfze4P9EgxNuyk7+xDGFtAYzAPBgNVHRMBAf8EBTADAQH/MA0GCSqGSIb3
DQEBCwUAA4ICAQAKHomtmcGqyiLnhziLe97Mq2+Sul5QgYVwfx/KYOXxv2T8ZmcR
Ae9XFhZT4jsAOUDK1OXx9aZgDGJHJLNEVTe9zWv1ONFfNxEBxQgP7hhmDBWdtj6d
taqEW/Jp06X+08BtnYK9NZsvDg2YRcvOHConeMjwvEL7tQK0m+GVyQfLYg6jnrhx
egH+abucTKxabFcWSE+Vk0uJYMqcbXvB4WNKz9vj4V5Hn7/DN4xIjFko+nREw6Oa
/AUFjNnO/FPjap+d68H1LdzMH3PSs+yjGid+6Zx9FCnt9qZydW13Miqg3nDnODXw
+Z682mQFjVlGPCA5ZOQbyMKY4tNazG2n8qy2famQT3+jF8Lb6a4NGbnpeWnLMkIu
jWLWIkA9MlbdNXuajiPNVyYIK9gdoBzbfaKwoOfSsLxEqlf8rio1GGcEV5Hlz5S2
txwI0xdW9MWeGWoiLbZSbRJH4TIBFFtoBG0LoEJi0C+UPwS8CDngJB4TyrZqEld3
rH87W+Et1t/Nepoc/Eoaux9PFp5VPXP+qwQGmhir/hv7OsgBhrkYuhkjxZ8+1uk7
tUWC/XM0mpLoxsq6vVl3AJaJe1ivdA9xLytsuG4iv02Juc593HXYR8yOpow0Eq2T
U5EyeuFg5RXYwAPi7ykw1PW7zAPL4MlonEVz+QXOSx6eyhimp1VZC11SCg==
-----END CERTIFICATE-----
subject=CN = SnakeOil
issuer=CN = SnakeOil
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 2103 bytes and written 373 bytes
Verification error: self-signed certificate
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 4096 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 18 (self-signed certificate)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 34914A3145BEA7989B5E8E2D4A5DA78A4B0D36D1A366D7635BA0BA2CED6262EC
    Session-ID-ctx:
    Resumption PSK: B78E3A3C9C15BEF089FA41210922C931C830BDEA9F408D2E3C823DA0942B40BC540866832C0E6EF8545960851157ADBA
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 43 87 d0 c4 a5 49 95 26-c8 3e eb 08 d7 47 78 ca   C....I.&.>...Gx.
    0010 - a7 9c c7 a3 e0 f5 d1 a7-15 a8 36 65 2e a3 34 e2   ..........6e..4.
    0020 - 5b a9 15 f4 56 e2 ca f8-18 7b 9e 09 81 8f e8 a2   [...V....{......
    0030 - e0 46 49 94 e9 17 70 98-05 60 0c c6 42 e4 51 b8   .FI...p..`..B.Q.
    0040 - 0f 74 44 6f 0d 9d 2b ed-92 a1 b4 8b 02 bb 32 b2   .tDo..+.......2.
    0050 - 92 75 f2 11 f6 42 b4 09-f4 e4 50 af ce 9c f3 48   .u...B....P....H
    0060 - 4d 4c 5d 35 35 1a c3 4f-c4 f7 28 f2 53 cd f1 3e   ML]55..O..(.S..>
    0070 - 31 08 97 42 93 cc 98 de-0f c6 1d 44 5c 45 ee bb   1..B.......D\E..
    0080 - 03 91 a7 7f 06 6f b7 0f-3a ee b4 16 9d 3a a9 d6   .....o..:....:..
    0090 - 6e 6e c3 00 a1 14 fe 15-a5 8d f4 df c3 c9 f1 f8   nn..............
    00a0 - e3 ad 32 03 90 e4 7f 03-c7 5a e7 94 03 7d a3 9c   ..2......Z...}..
    00b0 - e1 5f 79 17 4e e3 2c a9-f9 ab 56 90 e1 14 2b f4   ._y.N.,...V...+.
    00c0 - 9f 08 8b db 34 7f c7 ac-a0 8e 14 d6 56 39 66 20   ....4.......V9f
    00d0 - f9 ff 3c 99 b2 c9 29 c3-f1 c0 21 48 38 2a b7 e5   ..<...)...!H8*..

    Start Time: 1724912336
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 968695D51AFC3A1386173BFADDFF02FCD532D3CE964688DD8A838B740B1709AB
    Session-ID-ctx:
    Resumption PSK: 6D59970DF925045566604F982DF39956A5DE4BDB494A580AC40145D14FA79FC30F672773A46E504C59798000F5963796
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 43 87 d0 c4 a5 49 95 26-c8 3e eb 08 d7 47 78 ca   C....I.&.>...Gx.
    0010 - 65 0c 8c 02 21 52 0c 37-53 9d c5 6d 64 82 19 c8   e...!R.7S..md...
    0020 - e6 1a 4e da 9a 16 59 33-f3 28 31 bd ef 57 6e a3   ..N...Y3.(1..Wn.
    0030 - 71 64 2b 05 21 f0 47 60-5e 6c 0a e3 75 70 ca 5f   qd+.!.G`^l..up._
    0040 - d4 7e e5 03 cc 6a 54 9b-f1 fb aa 6b 9a 64 f8 2c   .~...jT....k.d.,
    0050 - a3 3e 4b 47 de aa f5 c3-36 ae 3d 6d a4 fd c6 5c   .>KG....6.=m...\
    0060 - 81 b2 ae 8f a1 8f f2 63-80 80 0b c0 e3 fe 30 27   .......c......0'
    0070 - 26 24 c9 cb f9 83 38 fe-59 37 aa 20 1d 7e 43 91   &$....8.Y7. .~C.
    0080 - 2d f9 67 d9 9e 67 e5 12-09 63 3d 34 4a c6 b3 2b   -.g..g...c=4J..+
    0090 - 2d ad c7 32 da 04 e6 6a-67 bc 9d 32 72 b8 f3 8c   -..2...jg..2r...
    00a0 - ad ef 59 f5 34 68 9c f0-db 6e b3 37 a0 5f 41 59   ..Y.4h...n.7._AY
    00b0 - 54 e5 89 b3 d8 ce 5c fa-d4 72 8a 79 76 72 be 47   T.....\..r.yvr.G
    00c0 - 16 c9 6e 38 a8 4c 59 7d-ff 0d 6e 43 37 66 ac 23   ..n8.LY}..nC7f.#
    00d0 - 8b 3a bb c3 34 99 59 7d-28 c7 6a 99 cb 8d 1e 16   .:..4.Y}(.j.....

    Start Time: 1724912336
    Timeout   : 7200 (sec)
    Verify return code: 18 (self-signed certificate)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

closed
bandit15@bandit:~$
```
## Solución
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx