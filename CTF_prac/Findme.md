# picoCTF Challenge: Redirection (HTTP Interception)

1. **Analyzing the Clues**: For this challenge, the clues provided were the username, password, and the phrase “any redirection?”. 
[The challenge](../ctf/fm1.png)
2. **First Look**: I checked the website, which redirected me to a "Search for flags" page. I tried searching for different terms, but it didn't return anything useful. Based on the clue, I realized the secret wasn't on the search page itself, but in the process of the redirection.
[The web](../ctf/fm2.png)
[The search for flag page](../ctf/fm3.png)
3. **Intercepting the Redirect**: I logged in again, but this time I used **Burp Suite** to capture the traffic. This allowed me to "freeze" the requests and see exactly what information was being passed between the server and my browser before the redirect finished.
[Using burpsuite](../ctf/fm4.png)
4. **Finding the Encoded Data**: While looking at the intercepted requests, I noticed a suspicious string in the `id=` parameter. It looked like **Base64** encoding, so I saved it and continued forwarding the requests.
[Finding the string](../ctf/fm5.png)
5. **Capturing More Fragments**: As I continued forwarding, I found another similar string. Once the redirection sequence ended and no more data appeared, I took those strings to a decoder.
[Another string](../ctf/fm6.png)
6. **Decoding the Flag**: I used a Base64 decoder on the strings I captured during the redirection phase. The decoded text revealed the flag.
[Decoding](../ctf/fm7.png)

**Final Flag**: `picoCTF{proxies_all_the_way_d1c0b112}`

---

### What I learned:
I learned that redirections can be used to hide information in plain sight. Because browsers follow redirects instantly, you can't see the data being passed in the URL parameters or headers without a tool like Burp Suite. This challenge also reinforced that Base64 is often used to pass data through URLs, but it offers no real security since it can be decoded by anyone.
