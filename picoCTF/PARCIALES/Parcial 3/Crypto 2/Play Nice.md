## Introducción
Not all ancient ciphers were so bad... The flag is not in standard format. `nc mercury.picoctf.net 33686` [playfair.py](https://mercury.picoctf.net/static/aec5fd7b1ec96307c4eda752a3353f68/playfair.py)
## Descripción
El cifrado Playfair es una técnica de cifrado simétrico manual y fue el primer cifrado de sustitución de digram literal.

La técnica encripta pares de letras (bigramas o digramas), en lugar de letras individuales como en los sistemas de cifrado de sustitución simple y Vigenère bastante más complejos que se utilizan en ese momento.
![[Pasted image 20241122225642.png]]
## Comandos

```

#!/usr/bin/python3 -u
import signal

SQUARE_SIZE = 6

def generate_square(alphabet):
	assert len(alphabet) == pow(SQUARE_SIZE, 2)
	matrix = []
	for i, letter in enumerate(alphabet):
		if i % SQUARE_SIZE == 0:
			row = []
		row.append(letter)
		if i % SQUARE_SIZE == (SQUARE_SIZE - 1):
			matrix.append(row)
	return matrix

def get_index(letter, matrix):
        for row in range(SQUARE_SIZE):
                for col in range(SQUARE_SIZE):
                        if matrix[row][col] == letter:
                            return (row, col)
        print("letter not found in matrix.")
        exit()

alphabet = "n5vgru7ehz1klja8s9340m2wcxbd6pqfitoy"
matrix = generate_square(alphabet)
msg = ""
enc_msg = "hnjm2e4t51v16gsg104i4oi9wmrqli"
for i in range(0, len(enc_msg), 2):
        a = get_index(enc_msg[i], matrix)
        b = get_index(enc_msg[i+1],matrix)
        if(a[0] == b[0]):
                msg += matrix[a[0]][(a[1]-1) % SQUARE_SIZE] + matrix[b[0]][(b[1]-1)% SQUARE_SIZE]
        elif(a[1] == b[1]):
                msg += matrix[(a[0]-1)% SQUARE_SIZE][a[1]] + matrix[(b[0]-1)% SQUARE_SIZE][b[1]]
        else:
                msg += matrix[a[0]][b[1]] + matrix[b[0]][a[1]]
        
print(msg)
```
## Solución 
dbc8bf9bae7152d35d3c200c46a0fa30