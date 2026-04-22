# picoCTF Challenge: Local-Authority (2FA Bypass)

1. **Introduction to Burp Suite**: For this challenge, it’s the introduction to Burp Suite. Burp Suite is a tool in Kali Linux that acts as a middleman between the client and the server. Burp Suite is useful, because you can see the request & response of a specific website and manipulate it real time to see how it would react. 
[The challenge](../ctf/intburp1.png)
2. **First Look**: First thing I did was checked the website, and as you can see, it’s a registration type. 
[The web](../ctf/intburp2.png)
3. **Intercepting Traffic**: Next thing I did was turned the interceptor on in Burp Suite, so it would send the request of the website that I will press. 
[turning intercept on](../ctf/intburp3.png)
4. **The 2FA Roadblock**: Now I tested the registration using “test” as the value of all, then it lead me to 2FA authentication. This time, I had a hard time on what to do, because I have to enter the OTP but there’s no clue anywhere what the OTP would be.
[The test](../ctf/intburp4.png)
5. **Analyzing the Request**: So what I did was try any random words to put in OTP so that it would send the request to Burp and so I can see if there’s anything I can manipulate in order to bypass the authentication. 
[The OTP](../ctf/intburp5.png)
6. **Using the Repeater**: Then I sent it to repeater so I could try to manipulate anything and so I can see how the web would respond.
[send to repeater](../ctf/intburp6.png)
7. **The Bypass**: And since this is a 2FA authentication I tried erasing the `OTP=test` in request to see how the web would react. 
[The manipulation](../ctf/intburp7.png)
8. **Capturing the Flag**: And then I found the flag. 

**Final Flag**: `picoCTF{#0TP_Bypvss_SuCc3$S_2e80f1fd}`

---

### How did it work?
When I removed the OTP in the backend, the web client thinks that I’ve successfully input the OTP since it disappeared, that’s why it showed me the FLAG. This is a logic flaw where the server doesn't check if the code is correct, but only checks if the process moved forward.
