# picoCTF Challenge: Insp3ct0r

This challenge is a lesson in thorough investigation. It requires inspecting all the core files that make up a website to find different pieces of a hidden flag.
[The Challenge](../ctf/in1.png)
### Steps I took:

1. **Initial Surface Check**: I started by looking at the live website for any visible clues, but nothing stood out immediately on the page itself.
[The website](../ctf/in2.png)
2. **Finding Part 1 (HTML)**: I opened the **Web Inspector** (F12) and looked through the HTML Elements. I found the first part of the flag hidden in an HTML comment.
[The first part](../ctf/in3.png)
3. **Finding Part 2 (CSS)**: Based on the hint that "CSS" was involved, I went to the **Sources** tab and opened the `.css` file linked to the page. There, I found the second part of the flag.
[The second part](../ctf/in4.png)
4. **Finding Part 3 (JavaScript)**: Finally, I checked the `.js` file. Just like the others, the third and final part of the flag was hidden in the code comments.
[The final part](../ctf/in5.png)
5. **Assembly**: After combining all three parts in order, I had the complete flag.
[The Flag](../ctf/in6.png)

---

### What I learned:
A website is not just what you see on the screen. It is a combination of Structure (**HTML**), Style (**CSS**), and Logic (**JavaScript**). As a security researcher, you have to check every single file the browser loads, because developers might split sensitive information across different files thinking no one will check them all.
