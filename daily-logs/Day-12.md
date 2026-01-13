## 📅 Day 12 – PicoCTF

- **Date:** 13 January, 2026  
- **Challenge:** Nice Netcat... 

### ✅ Challenge Solved
- **Name:** Nice Netcat...
- **Category:** General Skills
- **Difficulty:** Easy  

### 📜 Description
- In this challenge, we've to use the nc command to get output .
- Use the concept of ASCII to conert number to charachter .

### 🛠️ Commands Used
- `nc`
- ### `nc <hostname> <port> | awk '{for (i = 1; i <= NF; i++) printf"%c" $i}'`

### Concept Learned
- learned to identify what is used to encode the character.
- whether it is base64, ASCII, HEX etc . 
