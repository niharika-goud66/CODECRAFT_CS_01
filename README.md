# CODECRAFT_CS_01
Python implementation of the Caesar Cipher encryption and decryption algorithm.
def caesar_cipher(message, shift, mode):
    result = ""

    if mode == "decrypt":
        shift = -shift

    for char in message:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            new_char = chr((ord(char) - base + shift) % 26 + base)
            result += new_char
        else:
            result += char

    return result


message = input("Enter your message: ")
shift = int(input("Enter shift value: "))
mode = input("Enter encrypt or decrypt: ").lower()

if mode in ["encrypt", "decrypt"]:
    print("Result:", caesar_cipher(message, shift, mode))
else:
    print("Invalid choice! Enter encrypt or decrypt.")



Caesar Cipher Using Python

Project Overview

This project implements the Caesar Cipher algorithm using Python to encrypt and decrypt messages.

Features

- Encrypt messages using a shift value.
- Decrypt encrypted messages.
- Supports uppercase and lowercase letters.
- Preserves spaces and special characters.

Technology Used

- Python 3

How to Run

1. Install Python 3.
2. Download "caesar_cipher.py".
3. Open a terminal in the project folder.
4. Run:

python caesar_cipher.py

5. Enter the message, shift value, and operation.

Sample Output

Enter your message: Hello World
Enter shift value: 3
Enter encrypt or decrypt: encrypt
Result: Khoor Zruog

Learning Outcomes

Learned the basics of encryption, decryption, Python programming, and classical cryptography.

Disclaimer

Caesar Cipher is intended for educational purposes and is not secure for protecting sensitive information.
