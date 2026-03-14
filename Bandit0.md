# Bandit Level 0 Write-up

I’m starting to learn the basics of the command line. I'm using **overthewire.org**, where you move up to the next level every time you find the password. For this first challenge (**Bandit0**), I needed to find the password to proceed to Level 1.

### Steps I took:

1. **Checking the directory**
First, I checked my current directory to see where I was.
bash: pwd

2. **Listing File**
After that, I used the ls command to see the list of files within my directory. I saw that there was only one file: readme.
-bash: ls

3. **Reading files**
Once I found the readme file, I used the cat command to see if the password was inside.
bash: cat readme

4. **Result**
   I was able to find the password!
   Password: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If

**What I learned:**
The cat (concatenate) command is used for reading and displaying the content of files, or even combining multiple files into a single one.
