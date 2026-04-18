# picoCTF Challenge: Client-side-again

The clue for this challenge was "Never trust the client." This is a fundamental rule in web security: if the validation logic is sent to the user's browser (the client), the user can always see it, bypass it, or deconstruct it.
[The Challenge](../ctf/cl1.png)
### Steps I took:

1. **Initial Testing**: I started by trying random credentials in the login portal. It gave a standard "Incorrect password" alert, so I knew I needed to find the specific string the code was looking for.
[The web testing](../ctf/cl2.png)
2. **Inspecting the Source**: I opened the Web Inspector and found a JavaScript function that handled the login. The code was obfuscated (scrambled) and used a "split" variable to verify parts of the password at specific index positions.
[The scrambled flag](../ctf/cl3.png)
3. **Deciphering the Logic**: I analyzed the script and realized it was checking the input by slicing it into pieces. For example:
    * `(0, split)` where `split` is 4, meant the first 4 characters were `pico`.
    * `(24, 28)` meant the characters at those positions were `eb02`.
4. **Assembling the Flag**: By mapping out each segment based on the multiplication and position hints in the code, I pieced the fragments together manually until the full flag was formed.

**Final Flag:** `picoCTF{no_clients_plz_2eb02b45}`

---

### What I learned:
I learned that even if code looks like "gibberish" or a math puzzle at first, it can be solved by patiently tracing the logic. This reinforced the idea that **client-side validation is not real security** because the "secret" is technically already on my computer!
