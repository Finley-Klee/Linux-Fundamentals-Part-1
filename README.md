# Linux-Fundamentals-Part-1
A walkthrough of my learning on TryHackMe in the first of 3 rooms dedicated to learning the Linux OS. (https://tryhackme.com/r/room/linuxfundamentalspart1)

<h2>Description</h2>
This introductory TryHackMe room focuses on running basic commands on a Linux terminal, interacting with the file system, and understanding users and groups in Linux. Although it uses Linux Ubuntu, unlike other TryHackMe rooms which have a full Ubuntu desktop environment, this room deploys a Terminal only.

<h2>Utilities Used</h2>

- <b>Terminal</b> 

<h2>Environments Used </h2>

- <b>Linux Ubuntu</b>

<h2>Project walk-through:</h2>

- <b>Running Your First Few Commands</b>
<p>The first 3 tasks of the Linux Fundamentals 1 room provide background information about Linux and instructions on how to start the virtual machine to do the exercises. Now that I have read through that information I'm ready to start learning some commands.</p>
<br>
<p align="center">The first two commands taught in this room are "echo" and "whoami". To output the text "TryHackMe" I used the command echo TryHackMe. <br/>
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/9cf728ba-b965-4e4a-8663-792b927c2257" height="80%" width="80%" alt="a black background with white text. The text reads tryhackme@Linux1:~$ echo TryHackMe on the first line and below that a line which reads TryHackMe. Finally the last line reads tryhackme@Linux1:~$"/>
  <br />
  <br />
  Next, I used whoami to discover that the machine is logged in as user tryhackme. <br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/b22b7092-cf85-4ad7-ba2f-cecabac040b9" height="80%" width="80%" alt="a black background with white text. The text reads tryhackme@Linux1:~$ whoami on the first line and below that a line which reads tryhackme. Finally the last line reads tryhackme@Linux1:~$"/>
</p>
<br />
<br />
- <b>Interacting with the Filesystem</b>
<p>In this next section 4 new commands are introduced: ls, cd, cat, and pwd. </p>
<br>
<p align="center">To begin the section exercises I used ls to list the contents of the current directory (user tryhackme). Doing this I discovered that there are 4 folders.<br/>
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/bce54151-5854-4b17-b61f-8f3ba04b418a" height="80%" width="80%" alt="A black background with white and blue text. The first line in white reads tryhackme@Linux1:~$ ls. The next line has five items: access.log is written first in white followed by folder 1, folder 2, folder 3, and folder 4 all written in blue."/>
  <br />
  <br />
  The next question asks which folder has a text file in it, so I used the chnage directory (cd) command to navigate to each folder and the listing (ls) command to check for contents. In doing this I discovered a note.txt in folder 4.<br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/04506ad8-7d98-47a3-adba-4d825ef66e19" height="80%" width="80%" alt="A black background with white text. The first line ends with cd folder 1 after the username, then the next line ends with ls, the third line ends with cd ../folder 2 and the lines alternate like this until the ls in folder 4 results in a line which reads note.txt."/>
  <br />
  <br />
  I printed the contents of this file using the concatenate command (cat) and found that it read "Hello World!" <br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/51048565-6909-4853-9590-541c390f7e8c" height="80%" width="80%" alt="A black background with white text. The first line reads tryhackme@Linux1:~/folder4$ cat note.txt. The second line reads Hello World! and the last line reads tryhackme@Linux1:~/folder4$"/>
   <br />
  <br />
 Lastly, I used the print working directory (pwd) command to discover that the file's location is /home/tryhackme/folder4<br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/db301479-83e8-4362-ab55-e27c145c3fb3" height="80%" width="80%" alt="A black backgorund with white text. The first line reads tryhackme@Linux1:~/folder4$ pwd. The next line reads /home/tryhackme/folder4. The last line reads tryhackme@Linux1:~/folder4$"/>
</p>
<br />
<br />
- <b>Section Name</b>
<p>Description</p>
<br>
<p align="center">Step One: <br/>
  <img src="" height="80%" width="80%" alt="image one"/>
  <br />
  <br />
  Step Two: <br />
  <img src="" height="80%" width="80%" alt="image two"/>
  <br />
  <br />
  Step Three: <br />
  <img src="" height="80%" width="80%" alt="image three"/>
   <br />
  <br />
  Step Four: <br />
  <img src="" height="80%" width="80%" alt="image four"/>
   <br />
  <br />
  Step Five: <br />
  <img src="" height="80%" width="80%" alt="image five"/>
</p>
