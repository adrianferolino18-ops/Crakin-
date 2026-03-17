# picoCTF Challenge: Cookie Monster

This was an easy challenge from picoCTF. Because of the title "Cookie Monster" and the hints provided, I had a good idea of where to look.

**Steps I took:**

1. **Initial Test**: When I launched the challenge, I first tried to log in to see how the site would react. I got an "Access Denied" message, but it also gave me a clue to keep digging.
2. **Inspecting the Site**: I opened the browser's inspection tool to check the site's cookies. I found a cookie that looked suspicious because it was a long string of random characters.
3. **Decoding the Secret**: Since I recognized the format, I tried to decode the cookie using **Base64**. 

**Result:**
After decoding the cookie, the flag was hidden right inside.

[Check out the login attempt here](./ctf.cm.1.png)
[Check out the login attempt result here](./ctf.cm.2.png)
[View the cookie inspection here](./ctf.cm.3.png)
[See the decoded flag here](./ctf.cm.4.png)

---

**What I learned:**
Websites often use cookies to store session data, but sometimes they store sensitive information there too. Always check the **Application/Storage** tab in your browser tools to see what the site is saving on your computer.
