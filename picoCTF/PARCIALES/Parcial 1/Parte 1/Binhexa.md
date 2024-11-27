## Introducción
How well can you perfom basic binary operations?Start searching for the flag here `nc titan.picoctf.net 50534`

## Descripción

```
┌──(kali㉿kali)-[~]
└─$ nc titan.picoctf.net 50534

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 00001111
Binary Number 2: 01011001


Question 1/6:
Operation 1: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 

Incorrect input. Provide the right input
Enter the binary result: 0b1011111
Incorrect. Try again
Enter the binary result: ^C
                                                                                    
┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]
└─$ nc titan.picoctf.net 50534

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10100101
Binary Number 2: 10011110


Question 1/6:
Operation 1: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b10111111
Correct!

Question 2/6:
Operation 2: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 0b101001010
Correct!

Question 3/6:
Operation 3: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b101000011
Correct!

Question 4/6:
Operation 4: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 0b1001111
Correct!

Question 5/6:
Operation 5: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b110010111010110
Correct!

Question 6/6:
Operation 6: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b10000100
Correct!

Enter the results of the last operation in hexadecimal: 0x84

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d9a7ddd2}


┌──(kali㉿kali)-[~]
┌──(kali㉿kali)-[~]
└─$ python3 solvebh.py
Input number a: 10100101
Input number b: 10011110
Choose the binary operations: |
Binary result:  0b10111111
Choose the binary operations: <<
Choose number a or b: a
Binary result:  0b101001010
Choose the binary operations: +
Binary result:  0b101000011
Choose the binary operations: >>
Choose number a or b: b
Binary result:  0b1001111
Choose the binary operations: *
Binary result:  0b110010111010110
Choose the binary operations: &
Binary result:  0b10000100
Hexadecimal result: 0x84


def bin_operations(a, b, operations): if operations == '+': result = bin(a + b) elif operations == '-': result = bin(a - b) elif operations == '*': result = bin(a * b) elif operations == '>>': num = input("Choose number a or b: ") if num == 'a': result = bin(a >> 1) elif num == 'b': result = bin(b >> 1) else: print("Invalid number to choose") elif operations == '<<': num = input("Choose number a or b: ") if num == 'a': result = bin(a << 1) elif num == 'b': result = bin(b << 1) else: print("Invalid number to choose") elif operations == '&': result = bin(a & b) elif operations == '|': result = bin(a | b) else: print("Invalid operations") return(result) if __name__ == "__main__": a = input("Input number a: ") b = input("Input number b: ") a = int(a, 2) b = int(b, 2) for i in range(6): operations = input("Choose the binary operations: ") result = bin_operations(a, b, operations) print("Binary result: ", result) if i == 5: print(f"Hexadecimal result: {hex(int(result, 2))}")
```

## Solución 
picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d9a7ddd2}