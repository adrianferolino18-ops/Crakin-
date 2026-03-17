# Bandit Level 1 Write-up

In this level, the goal was to find the password for Level 2 stored in a file called `-` located in the home directory.

### Steps I took:

1. **Checking the directory**
I used `pwd` to confirm my location and `ls` to see the files.
bash: ls

2. **The Problem**
At first, I tried to print the password using only cat and -:
bash: cat -
It didn't work! This is because the filename is a hyphen/dash symbol (-). 
In Linux, a dash is often used to represent Standard Input (stdin), which tells
the cat command to wait for manual keyboard input instead of reading a file.

3. **The solution**
To fix this, I used cat ./- to provide a direct file path. This makes it clear to the system that 
I am targeting a literal filename in the current directory rather than giving a command instruction.
bash: cat ./-

**Result:**
I successfully bypassed the stdin issue and found the password!

Password: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx

**What I learned:**
When a filename starts with a special character (like a dash), you can use the relative path ./ to tell the terminal 
"look for a file with this name in this specific folder" so it doesn't get confused.
