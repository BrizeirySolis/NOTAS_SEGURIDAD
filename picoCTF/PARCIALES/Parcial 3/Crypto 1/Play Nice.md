## Introducción
Not all ancient ciphers were so bad... The flag is not in standard format. `nc mercury.picoctf.net 33686` [playfair.py](https://mercury.picoctf.net/static/aec5fd7b1ec96307c4eda752a3353f68/playfair.py)
## Descripción
1. Mira el código fuente y en la parte inferior se enlaza a [la página de Wikipedia para un cifrado de Playfair](https://en.wikipedia.org/wiki/Playfair_cipher)
    
2. Encuentra un decodificador de cifrado Playfair, como [DCode](https://www.dcode.fr/playfair-cipher). Pegar en el texto cifrado `y7bcvefqecwfste224508y1ufb21ld`y el alfabeto/clave `meiktp6yh4wxruavj9no13fb8d027c5glzsq`. Asegúrese de aumentar el tamaño de la rejilla a 6x6 para que todo el alfabeto se adapte.
    
3. Haga clic en "Descifrado" para obtener `WD9BUKBSPDTJ7SKD3KL8D6OA3F03G0`convertir esto a minúscula con `python -c "print('WD9BUKBSPDTJ7SKD3KL8D6OA3F03G0'.lower())"`para conseguir `wd9bukbspdtj7skd3kl8d6oa3f03g0`.
    
4. Pese el texto descifrado en el programa en el servidor para obtener la bandera: `Congratulations! Here's the flag: 2e71b99fd3d07af3808f8dff2652ae0e`.
## Comandos

## Solución 
