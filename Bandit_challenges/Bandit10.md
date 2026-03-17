# Bandit Level 10 Write-up

In this level, the password for Level 11 was stored in the file `data.txt`. The clue indicated that the file contains **Base64 encoded data**.

### Steps I took:

1. **Viewing the Encoded Data**
I used the `cat` command to view the contents of `data.txt`. Instead of a clear password, I found a string of characters that looked like this:
`VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2Zaa2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==`

2. **The Solution: Base64 Decoding**
I recognized that Base64 is an encoding scheme used to represent binary data in an ASCII string format. To retrieve the actual password, the data needed to be decoded.

3. **Decoding the Password**
I copied the encoded string and used a Base64 decoding tool to translate it back into plain text. 

*(Note: While I used an online decoder for this level, the same result can be achieved in the terminal using the command: `base64 -d data.txt`)*

### Result:
The decoded string revealed the password for the next level.

**Password:** `dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`

---

### What I learned:
**Base64** is not encryption; it is **encoding**. It is used to turn complex data into a simple text format. To read it, you simply need to decode it using the proper tool or command.
