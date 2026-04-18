# picoCTF Challenge: Scavenger Hunt

1. **The Goal**: For this challenge, the task is to find the scavenged flag hence the title: Scavenger Hunt.
[The Challenge](../ctf/sc1.png)
2. **First Look**: First, I checked the website, to see if I can find any clue and there was nothing special I found, except what the author used to make the site. [The website](../ctf/sc2.png)
3. **Part 1 (HTML)**: I checked the sources to see if I can find something. Then I found the first part of the flag in the HTML. [HTML source](../ctf/sc3.png)
4. **Part 2 (CSS)**: So next, I checked the CSS and JS code since there was a clue about it in the website. And I found the second part of the flag in the CSS. [CSS source](../ctf/sc4.png)
5. **Part 3 (robots.txt)**: When I checked the JS code, it wasn’t a flag part I found, instead it’s a clue about the last part of the flag. Since the clue says “indexing my website”, I thought about robots.txt, since indexing in web development, is how search engines discover pages. To prevent this, developers use a robots.txt file. I checked this file by adding /robots.txt to the URL. When I checked the robots.txt directory, I found the third part of the flag, and also a clue for the next part. [JS source ](../ctf/sc5.png)  
[robots.txt directory](../ctf/sc6.png)
6. **Part 4 (.htaccess)**: Next, I checked the Apache server directory and found the fourth flag part plus a new clue. An Apache Server is the software that hosts the site and handles user requests. I looked for the .htaccess file, which is a configuration file used to set folder rules like access permissions and redirects. Developers sometimes hide "backdoors" or clues here; if the directory is misconfigured, it reveals these files in a public list like a normal folder. [Apache server directory](../ctf/sc7.png)
7. **Part 5 (.DS_Store)**: Finally, I noticed a clue about "making websites on a Mac" and "storing information." This led me to look for the .DS_Store (Desktop Services Store) file. On macOS, this is a hidden file automatically created in every folder to store metadata, such as how icons are arranged. When developers upload their site directly from a Mac, they often accidentally include this file. I accessed it by adding /.DS_Store to the URL. In web security, this file is a common source of "information leakage" because it can reveal the names of other secret files in the directory. By checking this, I found the final part of the flag and completed the scavenger hunt. [The final part](../ctf/sc8.png)

**Final Flag**: `picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}`


---

### What I learned:
I learned that a "Scavenger Hunt" in web security means checking every configuration file possible. From basic code (HTML/CSS) to server settings (.htaccess) and even OS-specific metadata (.DS_Store), sensitive data can be scattered anywhere if the developer isn't careful about what they upload.
