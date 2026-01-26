## 📅 Day 25 – PicoCTF

- **Date:** 26 January, 2026  
- **Challenge:** heap 0

### ✅ Challenge Solved
- **Name:** heap 0 
- **Category:** Binary exploitation
- **Difficulty:** easy 

### 📜 Description
- Are overflows just a stack concern?
Download the binary here.
Download the source here.
Additional details will be available after launching your challenge instance. 
### 🛠️ Commands Used
- nc
### Concept Learned
-To understand it, imagine a parking lot (the Heap).

Allocation: The parking attendant (malloc) assigns Spot A to your car (the input buffer).

Contiguity: Immediately after Spot A, the attendant assigns Spot B to a VIP car (the "safe variable").

The Flaw: The attendant doesn't paint lines on the ground.

The Exploit: You drive a "stretch limousine" (your long input) into Spot A. Because it's too long, the back half of your limo smashes into Spot B, crushing the VIP car.

-In computer terms:

The program reserved 32 bytes for your input.

It reserved the very next memory addresses for the critical variable.

The function scanf (or gets / strcpy) didn't check if your input fits inside those 32 bytes. It just kept writing until it overwrote the neighbor.
