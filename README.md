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
