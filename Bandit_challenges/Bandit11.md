# Bandit Level 11 Write-up

In this level, the password for Level 12 is stored in `data.txt`. The clue stated that all lowercase (a-z) and uppercase (A-Z) letters had been **rotated by 13 positions** (ROT13).

### Steps I took:

1. **Understanding ROT13**
ROT13 is a simple substitution cipher that replaces a letter with the 13th letter after it in the alphabet. For example, 'A' becomes 'N', and 'B' becomes 'O'.

2. **The Solution: Using the `tr` Command**
To decode the file, I used the `tr` (translate) command. This command maps one set of characters to another.

**Command Used:**
bash
cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'

**Breakdown of the Command:**
cat data.txt: Reads the scrambled text.

tr: The translation tool.

'A-Za-z': This is the "source" set (the standard alphabet).

'N-ZA-Mn-za-m': This is the "target" set (the alphabet shifted by 13).

**Why use N-ZA-M instead of just N-Z?**
If we only told the computer N-Z, it would stop at Z. By using N-ZA-M, we are telling the computer to "wrap around"—once it hits Z, the next letter in the rotation is A, and the 13th letter from Z is M. This ensures the entire alphabet is mapped correctly.

**Result:**
The rotation was reversed, and the plain-text password was revealed.

Password: 7x16WNj7vS6NQvY9H6Y9Y9H6Y9Y9H6Y9

**What I learned:**
The tr command is a powerful way to manipulate text by mapping characters. ROT13 is a classic example of how encoding can be easily reversed if you know the "key" (in this case, the number 13).
