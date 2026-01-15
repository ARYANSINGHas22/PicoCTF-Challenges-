## 📅 Day 14 – PicoCTF

- **Date:** 15 January, 2026  
- **Challenge:** New Caesar

### ✅ Challenge Solved
- **Name:** New Caesar
- **Category:** Cryptography 
- **Difficulty:** Medium

### 📜 Description
-  found a brand new type of encryption, can you break the secret code? (Wrap with picoCTF{})
fegdeogdgecoeocgcgchcfcffccfca new_caesar.py
### 🛠️ Commands Used
-import string

# The alphabet used in the challenge (first 16 lowercase letters)
ALPHABET = string.ascii_lowercase[:16]
LOWERCASE_OFFSET = ord("a")

def b16_decode(cipher):
    plain = ""
    # Process two characters at a time to reconstruct one byte
    for i in range(0, len(cipher), 2):
        # Get the 4-bit values (indices in our alphabet)
        n1 = ALPHABET.index(cipher[i])
        n2 = ALPHABET.index(cipher[i+1])
        # Combine the two 4-bit nibbles into an 8-bit byte
        binary = (n1 << 4) | n2
        plain += chr(binary)
    return plain

def unshift(c, k):
    t1 = ord(c) - LOWERCASE_OFFSET
    t2 = ord(k) - LOWERCASE_OFFSET
    return ALPHABET[(t1 - t2) % len(ALPHABET)]

# --- REPLACE THIS WITH YOUR ACTUAL CIPHERTEXT ---
cipher = "mlnklfnknljflfmhjimkmhjhmljhjomhmmjkjpmmjmjkjpjojgjmjpjojojnjojmmkmlmijimhjmmj"

print("Trying all possible keys:")
for key in ALPHABET:
    try:
        # Step 1: Unshift the cipher using the current key
        decrypted_b16 = ""
        for char in cipher:
            decrypted_b16 += unshift(char, key)
        
        # Step 2: Decode the Base16 result
        result = b16_decode(decrypted_b16)
        
        # Print results that contain printable text
        if all(c in string.printable for c in result):
            print(f"Key '{key}': {result}")
    except:
        continue

### Concept Learned
- learned about b16 encryption and rot algorithm together  
