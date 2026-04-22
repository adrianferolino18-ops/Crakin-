# picoCTF Challenge: Login

1. **Understanding Cookies**: For this challenge, it’s about cookies. Cookies in web are useful and sometimes essential functions on the web. Cookies enable web servers to store stateful information (such as items added in the shopping cart in an online store). They can also be used to save information that the user previously entered into form fields, such as names, addresses, and passwords for subsequent use. 
[The Challenge](../ctf/com1.png)
2. **First Look**: First thing I did was checked the website, and as you can see, it’s a log-in type form. So from this clue, it tells me that the flag is 90% in the cookies.
[The log-in form](../ctf/com2.png)
3. **Checking for Cookie Data**: What I did next was checked if it would send something in Cookie if I try to log-in, so I use "test" as username and password. And it did send something. 
[check out the captured cookie value here](../ctf/com3.png)
4. **Decoding the Value**: Based from the value, it looks like a line of strings of base64, so I tried to decode it using base64decode.org, then there, I found the flag. 
[check out the base64 decoding process here](../ctf/com4.png)

**Final Flag**: `picoCTF{c00k1e_m0nster_l0ves_c00kies_4736F6CB}`

---

### What I learned:
I learned that developers sometimes use cookies to store session data or user information in an encoded format like Base64. While Base64 makes the data look like random strings, it is not a form of encryption, and anyone can easily decode it to see the original information (or the flag) hidden inside.
