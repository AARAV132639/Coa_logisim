# Insights & logs regarding phase 1 implementation

## Implementation 1: Basic Logic Gates

### What XOR actually means?

- AND asks: "Are both true?"

- OR asks : "Is at least one true?"

- XOR asks: "Are they different?"

**XOR is fundamentally difference detector. It produces 1 when input disagree**

### Hidden problem XOR solves

- Imagine two swithces controlling a light. Light should turn on when the switches are in different positions. 

- Here comes XOR in this scene. It naturally answers :
                                                        - Did something change?
                                                        - Are these bits different?
                                                        - Is there any odd number?

### Why arithmetic loves XOR

- Suppose you add binary numbers.

- Observe the sum bit.

- It is exactly XOR

Hence in a half adder: 
                    - Sum ---> A XOR B
                    - Carry ---> A AND B

- This is the first place XOR becomes indispensable. Without XOR building arithmetic units become much harder

### Why hardware designers love XOR

- Because its the cheapest way to compare bits. 

Hence, 
        - Equality checking
        - Comparators
        - Error detection
        - Arithmetic unit
    
    all depend on XOR

### XOR and Parity

1. 1 XOR 1 = 0
2. Two identical bits cancel each other: 1 XOR 1 XOR 1 = 1

- Odd count survies, even count disappears.

- This lets hardware answer: Was this number of 1s odd or even

- This is called *parity checking*

- Memory systems and communication protocols use this for error detection.

### Magical property

- XOR is reversible

o A XOR B = c

o C XOR B = A

- Because identical bits cancel each other.

- This single property powers huge parts of computing

### Why cryptography loves XOR

- Ciper = Data XOR key

- To decrypt: Cipher XOR key = Data

- Same operation for encryption and decryption.

### Final take away

- XOR answers "What is different?"

- This is why XOR appears everywhere:

o Adders            o Subtractors       o Comparators       o Error detection       o Encryption            oChecksums          o RAID storage systems      oProcessor ALUs         o Digital communication




