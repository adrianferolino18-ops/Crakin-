# picoCTF Challenge: Inspect HTML

This challenge was easy because the title was "Inspect HTML" and the clue asked, "What is the web inspector in web browsers?" This was a direct hint to look at the site's source code.

### Steps I took:

1. **Opening the Inspector**: I launched the website and right-clicked to "Inspect" the page (or used Ctrl+Shift+I).
2. **Finding the Password**: I looked through the HTML Elements and found the flag hidden inside the code.
[Check out the HTML inspector here](../ctf/ih.png)

---

### What I learned:
The **Web Inspector** is a powerful tool for seeing how a site is built. Even if a password isn't visible on the screen, it might still be sitting in the HTML comments or tags where the developer forgot to remove it.
