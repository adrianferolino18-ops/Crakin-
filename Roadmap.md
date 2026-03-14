# 🛡️ 4-Week Web Exploitation Roadmap (Beginner)

## WEEK 1 — How the Web & Linux Work (FOUNDATION)
**Goal:** Understand what happens when you visit a website and stop being scared of the terminal.

### 🐧 Day 1–2: Linux Basics (Very Important)
You should feel comfortable moving around.
* **Learn & practice:** `ls`, `cd`, `pwd`, `mkdir`, `rm`, `cp`, `mv`, `cat`, `less`, & `nano`
* **Understand:** * File paths (`/home`, `/etc`)
    * What `root` is
    * Why permissions matter
> 👉 **Practice daily in terminal. Don’t just read.**

### 🌐 Day 3–4: Networking Basics
You don’t need CCNA-level stuff — just essentials.
* **Learn:** IP addresses, DNS, Ports, and HTTP.
* **Commands to try:** ```bash
    ping google.com
    curl [http://example.com](http://example.com)
    ip a
    ```
* **Ask yourself:** “How does my request reach the server?”

### 🔍 Day 5–7: HTTP & Browser DevTools
This is where web hacking truly starts.
* **Learn:** GET vs POST, Request vs Response, Headers, Cookies, and Status codes (200, 302, 403, 500).
* **Do this:** Open Chrome → `F12` → **Network tab**. Log into a site and watch where the credentials go.

---

## WEEK 2 — Web Technologies (Attacker POV)
**Goal:** Understand how developers build insecure websites.

* **Day 8–9: HTML** — Focus on Forms, Input fields, Hidden fields, and `action`/`method` attributes.
* **Day 10–11: JavaScript Basics** — Learn client-side validation and the DOM. 
    * ⚠️ *Lesson: Client-side security ≠ real security.*
* **Day 12–14: Backend Basics** — I recommend **PHP**. Learn how login systems work and what SQL queries look like.

---

## WEEK 3 — Kali Linux & Web Tools
**Goal:** Use tools intentionally, not blindly.

* **Day 15–16: Kali Essentials** — Permissions (`chmod`), Processes (`ps`, `top`), and Services.
* **Day 17–18: Burp Suite (CRITICAL)** — This is your #1 tool. Learn to intercept, modify, and replay requests.
* **Day 19–21: Scanning Basics** — Learn `nmap`, `gobuster`, and `whatweb`.

---

## WEEK 4 — Real Web Exploitation (Legal Labs Only)
**Goal:** Exploit vulnerabilities and understand why they work.

### 🎯 Day 22–24: OWASP Top 10
Focus on: **SQL Injection, XSS, Authentication flaws, and IDOR.**

### 🧪 Day 25–30: Hands-On Labs
* [PortSwigger Academy](https://portswigger.net/web-security) (Highly Recommended)
* [TryHackMe](https://tryhackme.com/) (Web Fundamentals path)

---

## 🚫 What You Should NOT Do
* ❌ Don't run random Kali tools without knowing what they do.
* ❌ **Don't attack real websites.**
* ❌ Don't rely on auto-scanners.

## ✅ Success After 1 Month
You should be able to read raw HTTP requests, use Burp confidently, and understand why SQLi/XSS happen.

# 📚 WHERE TO STUDY (Exact Sources)
### 🐧 DAY 1–2: Linux Basics
* **BEST PRIMARY SOURCE:** [OverTheWire – Bandit](https://overthewire.org/wargames/bandit/)
    * *Goal:* Complete up to **Level 10**.
    * *Why:* You learn by doing. No fluff, just terminal practice.
* **SECONDARY (If confused):** [Linux Journey](https://linuxjourney.com/)
    * *Focus on:* Command Line, Filesystem, and Permissions.

### 🌐 DAY 3–4: Networking Basics
* **PRIMARY:** [TryHackMe – Network Fundamentals](https://tryhackme.com/path/outline/presecurity)
    * *Rooms:* Intro to Networking, What is Networking?, and HTTP in Detail.
* **ALTERNATIVE (Text-based):** [Mozilla HTTP Guide](https://developer.mozilla.org/en-US/docs/Web/HTTP)
    * *Focus on:* Requests, Responses, Methods, and Status codes.

### 🔍 DAY 5–7: HTTP & Web Basics
* **PRIMARY:** [PortSwigger Web Security Academy](https://portswigger.net/web-security)
    * *Start with:* HTTP basics, Requests & Responses, and Authentication.
    * 🔥 **Note:** This site is the gold standard for web hacking.

---

### 💻 WEEK 2: Web Technologies (Attacker POV)
* **HTML & JavaScript:** [MDN Web Docs](https://developer.mozilla.org/en-US/)
    * *Focus on:* HTML forms, Input fields, and JS form validation.
* **Backend Basics (PHP):** [W3Schools PHP Guide](https://www.w3schools.com/php/)
    * *Focus on:* `$_GET`, `$_POST`, and basic SQL queries. 
    * ⚠️ *Just understand the flow—don't try to become a dev yet.*

---

### 🛠️ WEEK 3: Kali Linux & Tools
* **KALI USAGE:** [Kali Linux Documentation](https://www.kali.org/docs/)
    * Use this for tool explanations and environment setup.
* **BURP SUITE:** [Burp Suite Academy](https://portswigger.net/burp/documentation/desktop/getting-started)
    * *Learn:* Intercepting requests, Repeater, and Intruder.

---

### 🎯 WEEK 4: Real Web Exploitation Practice
* **HANDS-ON LABS:** [PortSwigger Academy](https://portswigger.net/web-security)
    * *Focus Labs:* SQL Injection, XSS, Authentication, and IDOR.
* **STRUCTURED PATH:** [TryHackMe Beginner Web Path](https://tryhackme.com/path/outline/web)
    * *Rooms:* Web Fundamentals & OWASP Top 10.
