# picoCTF Challenge: Forbidden Paths (Path Traversal)

1. **Understanding Paths**: This challenge is about paths in a website. Website paths are the specific hierarchical locations of pages, files, or resources appearing in the URL after the domain name. The challenge is to access an absolute file path that the website is filtering. There are two types of paths:
   * **Relative Path**: A shortcut based on your current working directory (e.g., `usr/flag.txt`).
   * **Absolute Path**: The full, explicit address starting from the root (e.g., `/usr/share/nginx/html/flag.txt`).
[The challenge](../ctf/path1.png)
2. **Initial Attempt**: First thing I did was checked the website. Since it has a file reader, I tried reading the `/flag.txt` file, as the clue mentioned the flag is in this file.
[The web](../ctf/path2.png)
3. **Filter Restriction**: But as you can see, the website returned "Not Authorized." This means the site is filtering direct access to that specific file name or path.
[The file restriction](../ctf/path3.png)
4. **Testing Absolute Paths**: Since `/flag.txt` did not work, I tried using the absolute path clues (/usr/share/nginx/html/). I tried `././././flag.txt` but it said the file did not exist. This suggested the `flag.txt` might not be inside that specific root directory.
[The absolute path](../ctf/path4.png)
5. **Path Traversal Bypass**: I decided to use **Path Traversal** (or directory traversal). This is a vulnerability that allows attackers to access restricted files outside the web root folder by using `../` sequences to navigate the file system. 

6. **Finding the Flag**: I tried using path traversal for each path level to see if the flag was stored somewhere else. Eventually, I went outside of the root using `../../../../flag.txt` and found the flag. Since I was already at the top of the directory structure (the root), using more `../` sequences wouldn't change the result—it would still point to the same top-level location.
[The path traversal](../ctf/path5.png)

**Final Flag**: `picoCTF{7h3_p47h_70_5ucc355_e5fe3d4d}`

---

### What I learned:
I learned that even if a website blocks you from typing a direct file path, you can often "bypass" the filter by using `../` to move backwards through the server's folders. This shows that the server isn't actually protecting the file; it's only protecting the specific "address" or name I typed first.
