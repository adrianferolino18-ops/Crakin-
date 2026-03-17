# Bandit Level 3 Write-up

In this level, I learned about **hidden files** in Linux. Any file or folder that starts with a dot (`.`) is considered hidden and won't show up with a standard search.

### Steps I took:

1. **Navigating to the directory**
I moved into the `inhere` directory where the password was supposed to be.
bash: cd inhere

2. **The Problem**
When I tried using ls, it didn’t show anything. I even tried using cat on the directory itself, but it didn't return any data. It looked like the folder was completely empty.

3. **The Solution**
I used the ls -a command. The -a flag stands for "all", which tells Linux to show every file in the directory, including the hidden ones.
Bash: ls -a
Output: . .. .hidden
Once I saw the hidden file (starting with that dot), I was able to read it and find the password for the next level.
Bash: cat .hidden

**Result:**
I found the hidden password and can now proceed to Level 4!

Password: 2v79eySdbS9uCHnE2EnMQW7SSh7mAt0C

**What I learned:**
In Linux, files starting with a . are hidden by default to keep the workspace clean. To see them, you must use the -a flag with the ls command.
