# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
msg = input("Enter message: ")
key = input("Enter key: ")

enc = [ord(c) ^ ord(key[i % len(key)]) for i, c in enumerate(msg)]
print("Encrypted (hex):", ' '.join(f"{x:02X}" for x in enc))

dec = ''.join(chr(x ^ ord(key[i % len(key)])) for i, x in enumerate(enc))
print("Decrypted:", dec)
```


## Output:

![Screenshot 2025-05-15 083628](https://github.com/user-attachments/assets/f26e279e-76e4-4a40-b357-0ba3198c2116)

## Result:
  The program is executed successfully

