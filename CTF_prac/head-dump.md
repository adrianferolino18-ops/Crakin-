# picoCTF Challenge: Heap Dump

1. **Understanding Heap Dumps**: For this challenge, it introduces you to what heap dumps are and why it’s important to access them. A heap dump is a snapshot of an entire workspace at a specific moment in time. It is a binary file that contains everything the application knows right at that second.
[The challenge](../ctf/dump1.png)
2. **Exploring the Site**: First thing I did was checked the website. After exploring the website, I noticed that we were given an API endpoint. After checking all the links, I found nothing useful except in the **#API Documentation**.
[Exploring the web](../ctf/dump2.png)
3. **Finding the Endpoint**: It showed me the different API endpoints for the website, but what caught my attention was the last one: `/heapdump`. It was similar to the title of the challenge, so I tried accessing its endpoint by changing the URL from `/api-docs` to `/heapdump`.
[The API documentation endpoint](../ctf/dump3.png)
4. **Analyzing the File**: When I entered it, it downloaded a file. I tried looking at the contents of the file to see what I could find. As you can see, it gave a bunch of strings. By having access to this, you can see sensitive data such as passwords and usernames.
[The file](../ctf/dump5.png)
5. **Capturing the Flag**: Since this is a CTF, I tried searching for the flag within the binary data using the `grep` command. Using `grep "picoCTF"`, I found the flag hidden in the memory snapshot.
[The flag](../ctf/dump6.png)
**Final Flag**: `picoCTF{Pat!3nt_15_Th3_K3y_a485f162}`


---

### What I learned:
I learned that a Heap Dump is a powerful source of information. Because it captures the live memory of an application, it can store sensitive information in "plain text" that was supposed to be encrypted or hidden on the front end. Searching through these files with tools like `grep` or `strings` is a key part of memory forensics.
