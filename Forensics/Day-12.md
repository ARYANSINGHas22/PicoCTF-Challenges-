## 📅 Day 11 – PicoCTF

- **Date:** 10 February, 2026  
- **Challenge:** Matryoshka doll 
- **Category:** Forensics
- **Difficulty:** Medium

### 📜 Description
- File is hidden inside a file , try to extract them and find the flag.
### 🛠️ Commands Used
- binwalk <filename>
- binwalk -e <filename> --> -e for extracting the binary signature of file to detect the other types of file.
- cd <extrtacted file>
- ls
- repeat this process till you find the flag.txt.
