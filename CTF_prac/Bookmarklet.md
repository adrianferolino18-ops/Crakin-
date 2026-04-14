# picoCTF Challenge: Bookmarklet

This challenge introduced me to **Bookmarklets**, which are bookmarks that run JavaScript code instead of simply opening a website. The hint mentioned that web browsers have multiple ways to execute JavaScript, which led me to use the developer tools.

### Steps I took:

1. **Understanding the Clue**: The challenge explained that a Bookmarklet is just a small piece of JavaScript. Knowing this, I looked for the script on the provided webpage.
[Bookmarklet Challenge](./ctf/bk1.png)
2. **Accessing the Console**: I found the JavaScript code on the site. Instead of saving it as a bookmark, I opened my browser’s **Console Tab** (F12 or Ctrl+Shift+I).
[The code](./ctf/bk2.png)
4. **Executing the Code**: I pasted the JavaScript code directly into the console and hit Enter. 
5. **Capturing the Flag**: As soon as the script ran, it processed the data and displayed the flag directly on my screen.
[The Flag](./ctf/bk3.png)

### What I learned:
I learned that you don't always need to follow the "intended" way (like creating a bookmark) to run a script. The **Browser Console** is a powerful environment that lets you execute JavaScript on any page manually to see what it does.
