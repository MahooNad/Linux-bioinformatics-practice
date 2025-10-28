# Learning Unix/Linux on macOS

## Command 1: <pre>*bash* <br>echo $SHELL<br></pre>
**Purpose:** Shows which shell I'm using (like zsh, bash, etc.)  
**My output:** `/bin/zsh`

## Command 2: <pre>*bash* <br>uname -a<br></pre>
**Purpose:** Shows system and kernel info about my computer.  
**My output:** Darwin macOS-User.local 24.6.0 Darwin Kernel Version 24.6.0: Mon Jul 14 11:30:51 PDT 2025; root:xnu-11417.140.69~1/RELEASE_ARM64_T8112 arm64

## Command 3: <pre>*bash* <br>pwd<br></pre>
**Purpose:** Prints the current working directory (shows where I am).  
**My output:** My home directory

## Command 4: <pre>*bash* <br>ls -la<br></pre>
**Purpose:** Shows **everything** in my home directory, including hidden files.  
**My output:** A bunch of files, folders and configurations, plus the hidden files. 

## Command 5: <pre>*bash* <br>cd ~/documents/NGS<br></pre>
**Purpose:** Changes directory.  
**My output:** I am now in the directory I had created for training purposes, NGS.

## Command 6: <pre>*bash* <br>mkdir NGS_short_sequence<br></pre>
**Purpose:** Creates a new directory.  
**My output:** I created a directory named 'NGS_short_sequence'.

#### Command 5: <pre>*bash* <br>cd ~/documents/NGS/NGS_short_sequence<br></pre>

## Command 7: <pre>*bash* <br>touch readme.txt<br></pre>
**Purpose:** Creates file.   
**My output:** I created a file named 'readme.txt'.

## Command 8: <pre>*bash* <br>nano readme.txt<br></pre>
**Purpose:** Opens a simple txt editor in the terminal and allows me to write/edit notes in the readme.txt file.  
**My output:** I added some guidelines in the 'readme.txt' file about the 'Lines and explanations.md' file. (Ctrl+ O + Enter > save)

## Command 9: <pre>*bash* <br>cat readme.txt<br></pre>
**Purpose:** This will print the contents of the file to my terminal.   
**My output:** I can see all of the notes I added to readme.txt in the terminal.

## Command 10: <pre>*bash* <br>git add readme.txt<br></pre>
**Purpose:** This will tell git that I wanna add the readme.txt file to my GitHub profile.  
**My output:** -

## Command 11: <pre>*bash* <br>git commit -m "Update readme.txt with new info"<br></pre>
**Purpose:** This will save a snapshot of the staged changes with a message describing what I did.   
**My output:** -

## Command 12: <pre>*bash* <br>git push<br></pre>
**Purpose:** Send my commits to Github.   
**My output:** I see the readme.txt in my Github profile. 














