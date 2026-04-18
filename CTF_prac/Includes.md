# picoCTF Challenge: Includes

1. **The Goal**: For this challenge, the clue was “Is there more code than what the inspector initially shows?” [The Challenge](../ctf/inc1.png)
2. **Initial Inspection**: The first thing I did was checked the website and the HTML. And since I didn’t find anything, based on the clue “more code than what the inspector initially shows” I checked the CSS and JS code to see if I can find something—since their code is not initially shown in the HTML. [The web](../ctf/inc2.png)
3. **Finding Part 1**: So when I checked the CSS code, I found the first part of the flag. [The CSS source](../ctf/inc3.png)
4. **Finding Part 2**: And then when I checked the JS code, I also found the final part of the flag. [The JS source](../ctf/inc4.png)

**Final Flag**: `picoCTF{1nclu51v17y_1of2_f7w_2of2_b8f4b022}`

---

### What I learned:
I learned that the "Inspector" usually shows you the HTML elements first, but the full website is made of other files like `.css` and `.js`. To find "hidden" code, you have to look into the Sources tab or click the links to these external files because they aren't always visible just by looking at the main HTML page.
