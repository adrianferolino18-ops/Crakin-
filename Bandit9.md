# Bandit Level 9 Write-up

In this level, the password for Level 10 is stored in the file `data.txt`. The clue stated that the password is one of the few **human-readable strings** and is preceded by several `=` characters.

### Steps I took:

1. **The Problem: Binary "Garbage"**
When I first tried to view the file, it was filled with non-readable characters and binary data. Standard tools like `cat` were not helpful because the password was buried inside a file meant for computers, not humans.

2. **The Solution: `strings` and `grep`**
I used the `strings` command, which is specifically designed to find and print sequences of printable characters in a binary file. To narrow down the results based on the clue, I piped the output into `grep`.

**Command Used:**
bash
strings data.txt | grep "=="

**Breakdown of the Command:**
strings: This command scans the file and ignores all the binary code, displaying only the text that a human can read.

| (The Pipe): This took all the readable lines found by strings and passed them to the next tool.

grep "==": This filtered those readable lines to only show the ones containing the = characters mentioned in the clue.

**Result:**
The terminal filtered out all the noise and showed the exact line containing the password.

Password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

**What I learned:**
When a file looks like "garbage" in the terminal, it's likely a binary file. The strings command is the best way to extract hidden text from these files, and combining it with grep makes it easy to find specific patterns.
