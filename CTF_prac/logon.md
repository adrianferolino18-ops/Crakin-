# picoCTF Challenge: Cookies (Bypass)

For this challenge, it’s about bypassing the log-in menu by manipulating the cookie value.
[The challenge](../ctf/log1.png)
### Steps I took:

1. **Initial Login Attempt**: What I did first was log-in using "Joe" as username and "test" as password to see what value it would return and it returned nothing.
[The web](../ctf/log2.png)
2. **Testing Values**: What I did next was try testing other usernames and passwords, and I did get something in the cookie.
[The test](../ctf/log3.png)
3. **Manipulating the Cookie**: Then I tried manipulating the value admin "False" to "True".
4. **Getting the Flag**: Then when I refreshed it, I found the flag.
[The flag](../ctf/log4.png)

---

### What I learned:
I learned that you can bypass a login menu just by changing the data the website saves in your browser. If the "admin" check is only done through a cookie that the user can edit, it's very easy to trick the site.
