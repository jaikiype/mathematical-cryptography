# RSA Encryption and Decryption Project

## Objective
This project demonstrates the implementation of the RSA encryption and decryption process. The aim is to explore the mathematical foundation of RSA, from key generation to encryption and decryption, ensuring secure communication. This work was completed as part of the **Cryptographic Mathematics (MA6011)** assignment.

---

## Overview

The project is divided into three main phases:

1. **RSA Key Generation**
   - Generation of two large prime numbers.
   - Calculation of modulus and Euler's totient.
   - Selection of public and private keys.
2. **RSA Encryption**
   - Preparation and segmentation of the plaintext.
   - Conversion of text into numerical format.
   - Encryption using the public key.
3. **RSA Decryption**
   - Decryption of ciphertext using the private key.
   - Reconstruction of the original plaintext.

---

## RSA Process Details

### Phase 1: Key Generation
- **Prime Generation:** Two large 300-digit primes (`p` and `q`) are generated using a random seed.
- **Modulus (n):** Calculated as \( n = p \times q \).
- **Euler's Totient (ϕ):** \( \phi(n) = (p - 1)(q - 1) \).
- **Public Exponent (e):** Set to 65537, a standard choice for efficiency and security.
- **Private Exponent (d):** Computed as the modular inverse of \( e \) modulo \( \phi(n) \).
- **Public Key:** \( (n, e) \) is shared for encryption.

### Phase 2: Encryption
- **Text Preparation:** Plaintext is divided into manageable segments.
- **ASCII Conversion:** Each segment is converted into integer form via ASCII encoding.
- **Encryption Formula:** \( c = m^e \mod n \), where \( m \) is the plaintext segment.
- **Concatenation:** Encrypted segments are concatenated and shared.

### Phase 3: Decryption
- **Cipher Splitting:** The received ciphertext is split into segments.
- **Decryption Formula:** \( m = c^d \mod n \), where \( c \) is the ciphertext segment.
- **Text Reconstruction:** Decrypted integers are converted back to ASCII to form the plaintext.

---

## Features
- **Prime Security:** Ensures primes \( p \) and \( q \) are sufficiently large and distinct to prevent factorization.
- **Segmented Encryption:** Enables manageable encryption and decryption of large texts.
- **Key Sharing:** Public and private key generation facilitates secure communication.

---

## How to Use
1. **Key Generation:**
   - Generate the RSA keys using large prime numbers.
   - Share the public key \( (n, e) \).

2. **Encryption:**
   - Encode your plaintext into ASCII format.
   - Encrypt using \( c = m^e \mod n \).

3. **Decryption:**
   - Decrypt the received ciphertext using \( m = c^d \mod n \).
   - Convert the resulting integers back into text.

---

## Tools and Technologies
- **Programming Language:** Python (or any language supporting modular arithmetic).
- **Mathematical Libraries:** For generating large primes and performing modular arithmetic.

---

## Author
This project was completed by **Jaik Iype** and **Group 5** (in collaboration with Group 6) as part of the **Cryptographic Mathematics (MA6011)** course.
---

## References
- RSA Algorithm Documentation
- Cryptographic Mathematics Course Material
