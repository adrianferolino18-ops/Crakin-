# picoCTF Challenge: Local Authority

The clue for this challenge was: "How is the password checked on this website?" This immediately told me I needed to look at the logic behind the login form.

### Steps I took:

1. **Initial Inspection**: I started by inspecting the main page's HTML, but I didn't see anything strange there.
2. **Finding the Directory**: I tried to log in with random credentials, which redirected me to a login directory that said "log-in failed."
3. **Analyzing the Source**: I inspected that "failed" page and noticed a JavaScript file named `secure.js`. When I checked the source code of that file, I found the hardcoded username and password sitting right there.
4. **Getting the Flag**: I went back to the login page, entered the credentials I found in the script, and was able to see the flag.

### Results:
[Check out the login page here](./ctf/la.1.png)
[Check out the login failure page here](./ctf/la.2.png)
[Check out the secure.js source code here](./ctf/la.3.png)
[Check out the final flag here](./ctf/la.4.png)

---

### What I learned:
Never trust "Client-Side" security. If a password check is done in a `.js` file, anyone can use the browser's developer tools to see exactly what the password is!
