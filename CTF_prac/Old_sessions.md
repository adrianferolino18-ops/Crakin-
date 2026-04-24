# picoCTF Challenge: Session Hijacking (Sessions)

1. **The Goal**: This challenge demonstrates how proper session timeout controls and session privacy are critical for securing user accounts. 
[The Challenge](../ctf/os1.png)
2. **Finding the Leak**: I checked the website and saw a standard login form. I registered and logged in with "test" as my username and password to explore the site. On the homepage, I found a suspicious comment mentioning `/sessions`. 

3. **Exploring the Endpoint**: I visited the `/sessions` endpoint and found a list of active login sessions. This included session IDs and cookie values for various users. The most important one I noticed was the entry for the **admin**.
[The session endpoint](../ctf/os2.png)
4. **Cookie Manipulation**: I opened my browser's developer tools to check my own Cookies. Since my current session cookie identified me as the "test" user, I replaced my cookie value with the one I found for the admin in the `/sessions` list.

5. **Capturing the Flag**: After swapping the cookie value and refreshing the homepage, the server recognized me as the admin and displayed the flag.
[The flag](../ctf/os3.png)

**Final Flag**: `picoCTF{s3t_s3ss10n_3xp1rat10n5_53a328ed}`


---

### What I learned:
I learned that session IDs are like temporary keys to an account. If a developer accidentally makes a list of these keys public (like in a `/sessions` directory), an attacker can steal a key and "hijack" any account, including the admin, without ever needing a password.
