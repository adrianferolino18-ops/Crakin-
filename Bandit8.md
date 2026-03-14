# Bandit Level 8 Write-up

In this challenge, the password for Level 9 is stored in the file `data.txt` and is the only line of text that occurs exactly once.

### Steps I took:

1. **The Problem**
The file contains a vast number of lines where almost every entry occurs multiple times. I needed to find the single line that was unique.

2. **The Initial Attempt**
I knew that the `uniq -u` command is designed to filter out duplicates and display only unique entries. However, running `uniq -u data.txt` directly failed. 

3. **The Solution: Sorting and Piping**
I discovered that the `uniq` command only detects duplicate lines that are positioned immediately next to each other. Because the redundant passwords in this file were scattered throughout, `uniq` missed them. 

To fix this, I had to use two commands together:
* **`sort`**: This organizes the data into alphabetical order, forcing all identical lines to be adjacent.
* **`|` (The Pipe)**: This takes the output of the first command and sends it as input to the second.

**Command Used:**
bash
sort data.txt | uniq -u

**Breakdown of the Command:**
sort data.txt: Alphabetizes every line in the file so duplicates are grouped together.

|: Pipes the sorted list into the next command.

uniq -u: Scans the sorted list and "vaporizes" any line that appears more than once, leaving only the single unique password.

**Result:**
By combining these tools, I successfully isolated the unique password from the thousands of duplicates.

Password: 4CKMh1JI9lbUIZZPXDqGanal4xvAg0JM

**What I learned:**
The uniq command is powerful but has a limitation: it only looks at adjacent lines. Always pair it with sort when you need to find unique items in an unsorted list.
