# Bandit Level 5 Write-up

In this level, I dealt with a directory containing a massive amount of subdirectories and files. The goal was to find a specific file that matched these criteria:
* Human-readable
* 1033 bytes in size
* Not executable

### Steps I took:

1. **The Challenge**
The `inhere` directory contained dozens of subdirectories, each with its own files. Searching through these manually would have been an exhausting task.

2. **The Discovery: The `find` Command**
Instead of manual checking, I used the `find` command to scan the entire directory tree at once.

**Command Used:**
bash
find . -type f -size 1033c ! -executable

Breakdown of the Command:
.: Tells the system to start searching "right here" in the current location and look through every folder underneath it.

-type f: Tells the system to ignore folders and only look for actual files.

-size 1033c: Searches for the exact file size specified in the instructions (the c stands for bytes).

!: This acts as a "NOT" operator.

! -executable: Used to filter out any files that were meant to be programs/executable, leaving only the data file.

3. **Locating the Password**
The command immediately identified the file path: ./maybehere07/.file2. I then used cat to read it and retrieve the password.
Bash
cat ./maybehere07/.file2

**Result:**
Using the find command saved me from the tiring work of manually checking every single subdirectory.

Password: HWasnPhtq9AVKe0dmk45n5STXcl79Y9W

**What I learned:**
The find command is essential for navigating complex file systems. By combining specific flags like -size and the ! (not) operator, you can filter thousands of files in a single second.
