# Bandit Level 7 Write-up

In this level, the password for Level 8 was stored in a file called `data.txt`, right next to the word **"millionth."**

### Steps I took:

1. **The Problem**
At first, I thought this would be a simple task of reading the file. However, when I tried to look at the content, I was met with a massive, long list of strings. Scrolling through it to find one specific word was impossible.

2. **The Solution: Using `grep`**
I used the `grep` command to filter the data. The **`grep`** command is used to search for specific words, phrases, or patterns inside text files and display only the matching lines on the screen.

**Command Used:**
bash: grep "millionth" data.txt

**Breakdown of the Command:**
grep: The search tool.

"millionth": The specific keyword I was looking for.

data.txt: The file the system should search through.

**Result:**
The terminal instantly ignored the millions of other lines and showed me exactly what I needed:

Password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc

**What I learned:**
When dealing with large files, don't try to read everything. Use grep to pull out the specific piece of information you need based on a keyword or pattern.
