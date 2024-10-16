## Objetivo
Decodificar la bandera que se muestra en el archivo python 
## Datos Otorgados
```
from hidden import flag, shift

def encode(data, shift):
	enc = ''
	for _ in data:
		enc += chr((ord(_)+shift) % 0xff)
	return enc

assert encode(flag, shift) == '-3(.4?B,5*9@7;065&0:&:6&-(5*@D'
```
## Resolucion
```´
def decode(encoded_data, shift):
    dec = ''
    for char in encoded_data:
        dec += chr((ord(char) - shift) % 0xff)
    return dec


encoded_flag = '-3(.4?B,5*9@7;065&0:&:6&-(5*@D'


for shift in range(1, 256):
    decoded_flag = decode(encoded_flag, shift)
    print(f"Shift {shift}: {decoded_flag}")

```
agrege un bucle para probar desplazamientos hasta encontrar uno legible 
## Ejecución
```
Shift 196: hncioz}gpet{rvkqpakuauqahcpe{
Shift 197: gmbhny|fodszqujpo`jt`tp`gbodz~
Shift 198: flagmx{encryption_is_so_fancy}
Shift 199: ek`flwzdmbqxoshnm^hr^rn^e`mbx|
Shift 200: dj_ekvyclapwnrgml]gq]qm]d_law{
```
## Solución
flagmx{encryption_is_so_fancy}