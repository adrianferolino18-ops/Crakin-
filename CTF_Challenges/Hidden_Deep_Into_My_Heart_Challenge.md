# My First CTF Experience: Web Exploitation on TryHackMe

This was my first time exploring TryHackMe and trying out a CTF challenge. Since it was my first time, I learned a lot. I only had knowledge about accessing directories and subdirectories, so I had a hard time figuring out how to solve this. I didn't know where to find the directories or hidden files of a web server, and it didn't help that I only had 1 hour each day to solve it.

### Finding a Shortcut: Gobuster
It took me a lot of tries until I discovered the **gobuster** command. This tool lists hidden directories, files, DNS, and subdomains on web servers. Once I learned about this command, I was able to solve the challenge quickly.

**The command I used:**
bash
gobuster dir -u [the url] -w /usr/share/dirb/wordlists/common.txt

**What the parts mean:**
dir: Stands for directories, since that’s what I was looking for.

-u: For the URL.

-w: For the wordlist. (A wordlist is just a list of words used for cracking passwords or finding files and directories).

**How I Solved It:**
Finding robots.txt: Using the command above, I found a hidden file called robots.txt.

**Checking the URL:** I added /robots.txt to the URL and found a clue—a password and a user.

**Exploring "Disallow":** I wasn't sure what "disallow" meant at first, so I just tried adding it to the URL. It led me to another part of the site that said "there's more to discover."

**The Final Scan:** I ran Gobuster again on that new URL and found the /admin directory.

**Admin Access:** I searched that directory in my browser and it led me to the admin login. That’s how I finally solved the challenge!

**Reflection**
Even though the challenge said it was "easy," it was actually hard for me to figure out. I didn't have anyone to ask for help, so I just searched everything online. I’m starting to learn a lot of new things about web exploitation now.
