4-Week Web Exploitation Roadmap (Beginner)
WEEK 1 — How the Web & Linux Work (FOUNDATION)
Goal:
Understand what happens when you visit a website and stop being scared of the terminal.
Day 1–2: Linux Basics (Very Important)
You should feel comfortable moving around.
Learn & practice: bash
ls, cd, pwd, mkdir, rm, cp, mv, cat, less, & nano
Understand:
•	File paths (/home, /etc)
•	What root is
•	Why permissions matter
👉 Practice daily in terminal. Don’t just read.
Day 3–4: Networking Basics
You don’t need CCNA-level stuff — just essentials.
Learn:
•	What is an IP address
•	What DNS does
•	What a port is
•	What HTTP is
Commands to try: bash
ping google.com
curl http://example.com
ip a
Ask yourself:
	“How does my request reach the server?”
Day 5–7: HTTP & Browser DevTools
This is where web hacking truly starts.
Learn:
•	HTTP methods (GET, POST)
•	Request vs Response
•	Headers
•	Cookies
•	Status codes (200, 302, 403, 500)
Do this:
•	Open Chrome → F12 → Network tab
•	Log into any website
•	Watch:
o	Where username/password go
o	What cookies are set
🔥 If you master this, everything later clicks.
WEEK 2 — Web Technologies (Attacker POV)
Goal:
Understand how developers build insecure websites.
Day 8–9: HTML
Learn:
•	Forms
•	Input fields
•	Hidden fields
•	Action & method
👉 Look at page source of login pages.
Day 10–11: JavaScript Basics
Learn:
•	Client-side validation
•	How JS can be bypassed
•	DOM basics
⚠️ Important lesson:
Client-side security ≠ real security
Day 12–14: Backend Basics (Pick ONE)
I strongly recommend PHP for web exploitation beginners.
Learn concepts (not mastery):
•	How login systems work
•	How user input reaches the database
•	What SQL queries look like
You’re learning how bugs are born.
WEEK 3 — Kali Linux & Web Tools (Now It’s Useful)
Goal:
Use tools intentionally, not blindly.
Day 15–16: Kali Linux Essentials
Learn:
•	File permissions (chmod)
•	Processes (ps, top)
•	Services
You should understand why a tool needs root.
Day 17–18: Burp Suite (VERY IMPORTANT)
This is your #1 tool for web exploitation.
Learn:
•	Intercept requests
•	Modify parameters
•	Replay requests
•	Read raw HTTP
👉 Spend time here. This skill pays forever.
Day 19–21: Scanning Basics
Learn tools (lightly):
•	nmap
•	gobuster / dirsearch
•	whatweb
Understand:
•	What they find
•	What they can’t find
WEEK 4 — Real Web Exploitation (Legal Labs Only)
Goal:
Exploit vulnerabilities and understand why they work.
Day 22–24: OWASP Top 10 (Start Here)
Focus on:
•	SQL Injection
•	XSS
•	Authentication flaws
•	IDOR
For each:
•	Cause
•	Impact
•	Manual exploitation

Day 25–30: Hands-On Labs
Start with:
•	PortSwigger Web Security Academy ⭐⭐⭐
•	TryHackMe (Web Fundamentals path)
Rule:
If you don’t understand it → slow down → learn why.
What You Should NOT Do (Seriously)
•	❌ Don’t run random Kali tools
•	❌ Don’t attack real websites
•	❌ Don’t rely on auto scanners
•	❌ Don’t compare yourself to pros online
What Success Looks Like After 1 Month
You should be able to:
•	Read raw HTTP requests
•	Use Burp confidently
•	Understand why SQLi/XSS happen
•	Know what to test on a login page
•	Feel less “lost”
