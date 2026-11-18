# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM

### Name: M.Vetrivel
### Register Number: 212225040487
### Date: 18-11-2026

# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:
```c
#include <stdio.h>
#include <string.h>
void xor_encrypt_decrypt(char *input, char *key) {
    int input_len = strlen(input);
    int key_len = strlen(key);
    for (int i = 0; i < input_len; i++) {
        input[i] = input[i] ^ key[i % key_len];
    }
}
int main() {
    char url[] = "M.VETRIVEL";
    char key[] = "secretkey";
    printf("Original text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Encrypted text: %s\n", url);
    xor_encrypt_decrypt(url, key);
    printf("Decrypted text: %s\n", url);
    return 0;
}
```

# OUTPUT:
![alt text](<Screenshot 2026-11-18 141712.png>)

# RESULT:
Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption is executed sucessfully.


