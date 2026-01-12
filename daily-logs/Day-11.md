## 📅 Day 11 – PicoCTF

- **Date:** 12 January, 2026  
- **Challenge:** Mod 26  

### ✅ Challenge Solved
- **Name:** Obedient Cat  
- **Category:** Cryptography  
- **Difficulty:** Easy  

### 📜 Description
- In this challenge, we are given a file named `flag`.
- The task is to access and read the contents of the file using the command line.

### 🛠️ Commands Used
- `rot13`
- `cat`

###Concept Learned
- Wrap around modulo 
- 26 letter (A-Z)
- A->0, B->1....Z->25
- Plaintext: Z ; Shift = +3
- Z-> 25 then Z-> 28
- 28Mod26 = 2 therefore Z = 2 this is how wrap around modulo works.
