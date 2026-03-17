# Bandit Level 4 Write-up

In this level, the goal was to find the password for Level 5 stored in the only human-readable file within the `inhere` directory.

### Steps I took:

1. **The Manual Struggle**
At first, I realized there were many files in the `inhere` directory. Looking through them one by one to see which one contained the password was tiring and inefficient.

2. **The Discovery: Using `file` and Wildcards**
I learned that there is a better way to identify files without opening them. I used the command:
bash: file ./*

Breakdown of the Command:
file: This command identifies the type of file by examining its actual content rather than relying on the extension (like .txt or .docx).

The Asterisk (*): This is a wildcard in Linux. It acts as a powerful filter, allowing me to handle all files in the directory at once without typing each name manually.

3. **Finding the Target**
The file command showed that most files were just "data" (binary/garbage), but file07 was identified as ASCII text.

4. **Reading the Password**
Once I identified the correct file, I used cat to read it:
Bash: cat ./-file07

**Result:**
By using the right tools, I saved time and found the password instantly!

Password: 4oQYVPkxZOOE005pTW81FB8j8lxXGUQw

**What I learned:**
Instead of guessing, use the file command to see what you're dealing with. Wildcards like * are essential for performing actions on groups of files simultaneously.
