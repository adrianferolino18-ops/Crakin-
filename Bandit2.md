# Bandit Level 2 Write-up

In this level, the goal was to find the password for Level 3 stored in a file called `spaces in this filename` located in the home directory.

### Steps I took:

1. **Locating the file**
I used `ls` to see the files in my directory.
bash: ls

Output: spaces in this filename

2.**The Problem**
I tried to print the content of the file, but it didn't recognize it. The terminal only read the word spaces and ignored the rest:
Bash
cat spaces in this filename
Because of the spaces, the computer thought I was trying to open four separate files: spaces, in, this, and filename.

3. **The Solution**
I found out that there are two main ways to fix this:

Quotation Marks: Putting the whole name in " " or ' ' so the system reads it as one string.

Backslashes (\): Using a backslash before every space. This tells the system to treat the space as a character rather than a separator.

I used the backslash method in the terminal:
Bash
cat ./spaces\ in\ this\ filename

**Result:**
I was able to read the file and get the password!

Password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

**What I learned:**
Computers see spaces as "breaks" between instructions. To read a file with spaces in the name, you must escape the spaces using backslashes (\) or wrap the name in quotes.
