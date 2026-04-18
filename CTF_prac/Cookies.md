# picoCTF Challenge: Cookies

1. **The Goal**: For this challenge, it’s about cookies. [The challenge](../ctf/co1.png)
2. **Initial Testing**: First, I checked the website to see if there’s anything I could find, and since the title was about cookies, and the only thing that’s in the webpage is a return type value, I checked the clue that says “snickerdoodle” to see what value it would return. Then it returned a value of -1. [The website](../ctf/co2.png)
3. **Cookie Manipulation**: Then, I tried changing the value to zero, and found this, so I keep changing the value from 1, 2, 3, 4 and so on, until I found the flag. [The cookie manipulation](../ctf/co3.png)

**Final Flag**: `picoCTF{3v3ry1_l0v3s_c00k135_88acab21}`
[Flag](../ctf/co4.png)

---

### What I learned:
I learned that some websites use cookies to track which page or "session" you are viewing. By manually changing the numerical value of the cookie in the browser's inspection tool, I was able to cycle through different pages that I wasn't supposed to see until I found the one containing the flag.
