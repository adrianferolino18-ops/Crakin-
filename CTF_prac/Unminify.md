# picoCTF Challenge: Unminify

This challenge demonstrates **Minification**—the process where developers remove all extra spaces, tabs, and newlines from code to reduce file size and make it run faster for computers. While this makes the code hard for humans to read, the logic remains exactly the same.

### Steps I took:

1. **Initial Site Check**: I visited the website to see if there were any obvious clues or interactive elements, but the page appeared completely normal with no special features.
[Check out the minified HTML code here](../ctf/u1.png)
3. **Inspecting the Source**: Since I couldn't see anything on the surface, I opened the **Web Inspector** (F12) to look at the underlying HTML.
[The website](../ctf/u2.png)
5. **Finding the Flag**: Even though the HTML was minified (all bunched together in long lines), I was able to look through the tags and found the flag hidden directly in the source code.
[Check out the flag I found in the inspector here](../ctf/u3.png)


---

### What I learned:
I learned that **Minification is not Security**. Just because code is messy and hard to read doesn't mean it is protected. A security researcher can simply "unminify" the code or look closely at the Inspector to find exactly what they are looking for.
