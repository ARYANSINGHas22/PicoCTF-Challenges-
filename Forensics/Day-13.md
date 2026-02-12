## 📅 Day 13 – PicoCTF

- **Date:** 12 February, 2026  
- **Challenge:** like1000
- **Category:** Forensics
- **Difficulty:** Medium

### 📜 Description
- This challenge was similar to matryoshka doll , the difference is that , here there are 1000 file so we need a script.
### 🛠️ Commands Used
- tar -xvf <filename>
- script:
   Solver.py
   import tarfile
   import os
   i = 1000
   while i < 0:
   filename = f"{i}.tar"
   print("rxtracting file")

   try:
  with tarfile.open(filename) as tar;
  extractall();

  i -=1

  except:
  print(Successful or failed)
  break

  //code might have syntax error please do consider that.
