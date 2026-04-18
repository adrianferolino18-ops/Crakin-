# picoCTF Challenge: Forbidden Paths (robots.txt)

1. **The Challenge**: For this challenge, I kind of have an idea where the flag would be based on the title, description, and the hint.
[The challenge](../ctf/rob1.png)
2. **Checking robots.txt**: The first thing I did was inspect the website to see if there’s something I could find, but I didn’t find anything, so I proceed to go to robots.txt by adding `/robots.txt` to the URL. 
[The sources](../ctf/rob2.png)
   > **Note**: A `robots.txt` file is a standard practice to see which directories the developer wants to keep hidden from search engines. These 'Disallowed' paths often point to sensitive information or the flag itself.
[The robots.txt directory](../ctf/rob3.png)
3. **Finding the Hidden Path**: When I checked the robots.txt directory, I saw another clue. Since the `/cc6b1.html` is a HTML extension, I thought this would lead me to another webpage. 
4. **Capturing the Flag**: I followed that path and then I found the flag.
[The Flag](../ctf/rob4.png)

---

### What I learned:
I learned that developers use `robots.txt` to tell bots like Google what not to show in search results. However, for a security researcher, this file acts like a map that points directly to the folders the developer is trying to hide.
