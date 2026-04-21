# picoCTF Challenge: GET aHEAD

1. **Introduction to Burp Suite**: This challenge introduced me to Burp Suite. It’s a tool in Kali Linux that acts as a middleman between the client and server. With Burp Suite, I can see the request & response of a specific website and manipulate it in real time to see how the server reacts. It makes it much easier to read what’s happening behind the scenes.
[The challenge](../ctf/get1.png)

2. **Analyzing the Clues**: I checked the website and saw only two choices: Red and Blue. However, the clue said “maybe you have more than 2 choices,” and the title was “GET aHEAD.” This pointed toward **HTTP Methods**. In HTTP, methods indicate the action the request expects:
   * **GET**: Expects information back (like a website).
   * **POST**: Typically used when submitting information (like a login form).
   * **HEAD**: Similar to GET, but it only returns the headers and not the document body.
[The website](../ctf/get2.png)

3. **Intercepting Traffic**: I turned the **Intercept** on in Burp Suite to "listen" to my interactions with the web. When I pressed "Choose Blue," Burp Suite caught the request before it reached the server.
[check out the Burp Suite intercept here](../ctf/get3.png)

4. **Using the Repeater**: I sent the captured request to the **Repeater** tab so I could manipulate it and test different responses without having to click the button over and over.
[check out the Repeater manipulation here](../ctf/get4.png)

5. **Changing the Method**: Based on the "aHEAD" clue, I changed the request method from `POST` to `HEAD`. When I sent the modified request, the server responded with the flag in the header information.
[check out the flag in the response headers here](../ctf/get5.png)

**Final Flag**: `picoCTF{r3j3ct_th3_du4lity_8b13f07}`

---

### What I learned:
I learned that HTTP requests have different "verbs" or methods that change how a server responds. By using a proxy tool like Burp Suite, I can change these methods manually to uncover hidden data that isn't visible through a normal browser interaction.
