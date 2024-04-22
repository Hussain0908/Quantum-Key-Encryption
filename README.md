# Quantum Encryption with Quantum Key Distribution (QKD)

## Overview
This project implements a Quantum Key Distribution (QKD) protocol to generate secure keys for encryption and decryption, leveraging the principles of quantum mechanics. It includes functions for encryption and decryption of messages using the generated keys.

## Features
- Quantum Key Distribution (QKD) protocol implementation
- Encryption and decryption functions using generated keys
- Detection of eavesdropping attempts during key establishment phase
- XOR-based encryption and decryption for simplicity

## Requirements
- Python 3.x
- Cirq library (`pip install cirq`)

## Usage
1. Run the `QKD` function to generate secure keys for encryption and decryption.
2. Use the generated keys to encrypt and decrypt messages.

```python
# Generate keys using QKD protocol
alice_key, bob_key = QKD(num_bits)

# Encrypt message
encrypted_message = encrypt_message(message, alice_key)

# Decrypt message
decrypted_message = decrypt_message(encrypted_message, bob_key)



## Example
```python
from quantum_encryption import QKD, encrypt_message, decrypt_message

# Define unencrypted string
unencrypted_string = "This is a Test"

# Generate keys using QKD protocol
alice_key, bob_key = QKD(len(unencrypted_string) * 8)

# Encrypt message
encrypted_message = encrypt_message(unencrypted_string, alice_key)
print("Encrypted message:", encrypted_message)

# Decrypt message
decrypted_message = decrypt_message(encrypted_message, bob_key)
print("Decrypted message:", decrypted_message)
