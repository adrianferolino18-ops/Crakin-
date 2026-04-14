# picoCTF Challenge: WebDecode

The goal of this challenge was to use the web inspector to find a flag that might be hidden and potentially encoded in the site's source files.
[WebDecode Challenge](../ctf/wd1.png)
### Steps I took:

1. **Enumerating the Site**: Upon launching the site, I saw three main navigation paths: **Home**, **About**, and **Contact**.
[The Website](../ctf/wd2.png)
2. **Path Inspection**: I manually inspected the HTML source for every page. While the Home and Contact pages looked normal, the **About** page contained a suspicious string of random characters hidden within a `section` or `div` tag.
[Inspect](../ctf/wd3.png)
3. **Identifying the Encoding**: Recognizing the pattern of the string (which often ends in `=` or uses a specific character set), I suspected it was **Base64** encoded.
4. **Decoding for the Flag**: I copied the string and used a Base64 decoder. The decoded output revealed the flag.
[The Flag](../ctf/wd4.png)

---

### What I learned:
Developers sometimes hide data in "secondary" pages like the About or Contact sections, thinking people will only look at the main landing page. This challenge reinforced the habit of inspecting **every** file and path included in a web application.
