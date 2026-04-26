# picoCTF Challenge: More Cookies (Boolean Bypass)

1. **The Goal**: This challenge is about manipulating cookies to bypass authorization checks.
[The challenge](../ctf/pc1.png)
2. **Finding the Cookie**: First thing I did was checked the web, and I found a "Continue as Guest" button. Since this is about cookies, I tried clicking it to see if it would store a cookie in my browser.
[The web](../ctf/pc2.png)
3. **Identifying the Value**: It did store a cookie. What I did next was manipulate the cookie; I noticed a value called `isAdmin` (or a similar permission bit). Since the value was `0` (which represents **False**), I suspected this was what determined my access level.
[The testing](../ctf/pc3.png)
4. **The Swap**: I tried changing the value to `1` so the web would think I’m the admin (where `1` represents **True**). 

5. **Capturing the Flag**: After changing the value of the cookie to `1` and refreshing the page, the website recognized me as an administrator and revealed the flag.
[The manipulation](../ctf/pc4.png)

**Final Flag**: `picoCTF{gr4d3_A_c00k13_5d2505be}`

---

### What I learned:
I learned that using simple "True/False" flags in cookies is very insecure. If the server trusts the cookie sent by the browser without verifying it on the backend, any user can simply change their "Identity" or "Role" by flipping a single bit from 0 to 1.
