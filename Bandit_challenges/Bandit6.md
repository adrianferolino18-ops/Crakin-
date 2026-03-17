# Bandit Level 6 Write-up

In this challenge, the password was hidden somewhere on the **entire server**, not just in my home directory. The file had three specific properties:
* Owned by user `bandit7`
* Owned by group `bandit6`
* Exactly 33 bytes in size

### Steps I took:

1. **The Clue**
I checked my home directory with `ls`, but it was empty. This meant I had to search the entire system starting from the root directory (`/`).

2. **The Problem: Permission Denied**
I used the `find` command with the properties provided in the clue. However, because I was searching the whole server, my screen was flooded with "Permission denied" errors for folders I didn't have access to. It was almost impossible to see the actual result.

3. **The Solution: Redirecting Errors**
I searched for a way to clear the clutter and learned about `2>/dev/null`. 

**Command Used:**
bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null

**Breakdown of the Command:**
find /: Start searching from the root (top-level) directory.

-user bandit7 & -group bandit6: Filters for the specific owner and group.

2>/dev/null: This is the "clutter-clearer." In Linux:

2 stands for Standard Error (where error messages go).

> is the redirect symbol.

/dev/null is like a "black hole" that deletes everything sent to it.
This command told the system: "Show me the results, but throw all the errors in the trash."

4. **Retrieving the Password**
The command gave me one clean result: /var/lib/dpkg/info/bandit7.password. I then navigated to that directory and read the file.

Bash
cd /var/lib/dpkg/info/
cat bandit7.password

**Result:**
By silencing the errors, I found the one file on the whole server that belonged to me.

Password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

**What I learned:**
Using 2>/dev/null is essential when searching large systems. It allows you to ignore "Standard Error" and focus only on the data you actually have permission to see.
