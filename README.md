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
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/9cf728ba-b965-4e4a-8663-792b927c2257" width="80%" alt="a black background with white text. The text reads tryhackme@Linux1:~$ echo TryHackMe on the first line and below that a line which reads TryHackMe. Finally the last line reads tryhackme@Linux1:~$"/>
  <br />
  <br />
  Next, I used whoami to discover that the machine is logged in as user tryhackme. <br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/b22b7092-cf85-4ad7-ba2f-cecabac040b9" width="80%" alt="a black background with white text. The text reads tryhackme@Linux1:~$ whoami on the first line and below that a line which reads tryhackme. Finally the last line reads tryhackme@Linux1:~$"/>
</p>
<br />
<br />
- <b>Interacting with the Filesystem</b>
<p>In this next section 4 new commands are introduced: ls, cd, cat, and pwd. </p>
<br>
<p align="center">To begin the section exercises I used ls to list the contents of the current directory (user tryhackme). Doing this I discovered that there are 4 folders.<br/>
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/bce54151-5854-4b17-b61f-8f3ba04b418a" width="80%" alt="A black background with white and blue text. The first line in white reads tryhackme@Linux1:~$ ls. The next line has five items: access.log is written first in white followed by folder 1, folder 2, folder 3, and folder 4 all written in blue."/>
  <br />
  <br />
  The next question asks which folder has a text file in it, so I used the chnage directory (cd) command to navigate to each folder and the listing (ls) command to check for contents. In doing this I discovered a note.txt in folder 4.<br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/04506ad8-7d98-47a3-adba-4d825ef66e19" width="80%" alt="A black background with white text. The first line ends with cd folder 1 after the username, then the next line ends with ls, the third line ends with cd ../folder 2 and the lines alternate like this until the ls in folder 4 results in a line which reads note.txt."/>
  <br />
  <br />
  I printed the contents of this file using the concatenate command (cat) and found that it read "Hello World!" <br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/51048565-6909-4853-9590-541c390f7e8c" width="80%" alt="A black background with white text. The first line reads tryhackme@Linux1:~/folder4$ cat note.txt. The second line reads Hello World! and the last line reads tryhackme@Linux1:~/folder4$"/>
   <br />
  <br />
 Lastly, I used the print working directory (pwd) command to discover that the file's location is /home/tryhackme/folder4<br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/db301479-83e8-4362-ab55-e27c145c3fb3" width="80%" alt="A black backgorund with white text. The first line reads tryhackme@Linux1:~/folder4$ pwd. The next line reads /home/tryhackme/folder4. The last line reads tryhackme@Linux1:~/folder4$"/>
</p>
<br />
<br />
- <b>Searching for Files</b>
<p>Obviously searching manually through folders using cd and ls like in the previous section is inefficient and annoying, so the next section introduces the commands find and grep to make the search more manageable.</p>
<br>
<p align="center">If I wanted to find the location of the note.txt file in the previous section much faster, I could instead uses the find command and the wildcard with .txt to look through the 4 folders and print the location of the .txt file.<br/>
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/3f182797-87ce-416b-9c9a-5f92016a7673" width="80%" alt="A black backgorund with white text. The first line reads tryhackme@Linux1:~$ find -name *.txt. The next line reads ./tryhackme/folder4/note.txt. The last line reads tryhackme@Linux1:~$"/>
  <br />
  <br />
 However, the TryHackMe room actually asks us to use the grep command to search through the access.log file for a flag which will begin with THM. To find it I put THM followed by an * character in quotes between the grep command and the name of the file I wanted to search, in this case access.log. The output shows that the flag is THM{ACCESS}.<br />
  <img src="https://github.com/Finley-Klee/Linux-Fundamentals-Part-1/assets/171582741/00a1b3d2-d649-4e23-bf33-8c951a76086c" width="80%" alt="A black background with white text except for the term I searched for which is printed in red. The first line reads tryhackme@Linux1:~$ grep THM* access.log. The output from that command shows an ip address followed by a dat, followed by GET THM{ACCESS} followed by more information about the internet packet like the language, the browser, etc."/>
</p>
- <b>An Introduction to Shell Operators</b>
<p>In the last section we are introduced to the operators: &, &&, >, and >>. The difference between the & and && operators is their function. The & operator runs commands in the background so that you can continue using the terminal while the command is running, and the && operator allows you to combine commands together. The > and >> operators, however, differ in a more particular way. Both redirect the output of a command, but the > operator overwrites the contents if there are any there, while the >> operator adds the output to the end of any contents already there.</p>
<br>

