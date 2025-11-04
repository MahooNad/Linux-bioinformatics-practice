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

## Command 10: <pre>*bash* <br>git status<br></pre>
**Purpose:** This shows me if my origin/main and main are synced.  
**My output:** I see some files need to be updated on both sides.

## Command 11: <pre>*bash* <br>git pull origin main --rebase<br></pre>
**Purpose:** Downloads the latest commits from the remote main (origin/main), and re-applies any of my local commits on top of the changes.  
**My output:** -

## Command 12: <pre>*bash* <br>git add readme.txt<br></pre>
**Purpose:** This will tell git that I wanna add the readme.txt file to my GitHub profile.    
**My output:** -

## Command 13: <pre>*bash* <br>git commit -m "Update readme.txt with new info"<br></pre>
**Purpose:** This will save a snapshot of the staged changes, accompanied by a message describing the changes made.     
**My output:** -

## Command 14: <pre>*bash* <br>git push<br></pre>
**Purpose:** Send my commits to GitHub.     
**My output:** Everything up-to-date.

#### Command 6: <pre>*bash* <br>mkdir downloaded-data<br></pre>

## Command 15: <pre>*bash* <br>clear<br></pre>
**Purpose:** Clears the screen.   
**My output:** I'm on the first line in the terminal.(Phew! Thanks god! It's clean now!)

#### Command 5: <pre>*bash* <br>cd ~/documents/NGS/NGS_short_sequence/downloaded-data<br></pre>

## Command 16: <pre>*bash* <br>which fastq-dump<br></pre>
**Purpose:** Checks if I have the SRA toolkit installed.  
**My output:** fastq-dump not found.

## Command 17: <pre>*bash* <br>curl -O https://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-mac64.tar.gz<br></pre>
**Purpose:** Downloads the SRA Toolkit.  
**My output:** -

## Command 18: <pre>*bash* <br>tar -xvzf sratoolkit.current-mac64.tar.gz<br></pre>
**Purpose:** Extracts (x) the file 'sratoolkit.current-mac64.tar.gz' (f), shows the file being extracted (v), and uses zip compression (z).   
**My output:** -

#### Command 5: <pre>*bash* <br>cd sratoolkit.*/bin<br></pre>

## Command 19: <pre>*bash* <br>export PATH=$PATH:$(pwd)<br></pre>
**Purpose:** Adds the current folder, sratoolkit.*/bin, to the PATHs I have in my system.    
**My output:** -

## Command 20: <pre>*bash* <br>echo 'export PATH=$PATH:~/sratoolkit.*/bin' >> ~/.zshrc source ~/.zshrc<br></pre>
**Purpose:** This line makes the addition of the new PATH to the shell permanent, so I can always run commands like 'fasterq-dump' without the need to copy the full path.   
**My output:** -

## Command 21: <pre>*bash* <br>fasterq-dump --version<br></pre>
**Purpose:** Confirms the fasterq-dump is installed.  
**My output:** fasterq-dump : 3.2.1

## Command 22: <pre>*bash* <br>man tar<br></pre>
**Purpose:** The man command gives me the full manual of a command, like 'tar' in this case.   
**My output:** I can see the full manual. Exit with Q.

#### Command 5: <pre>*bash* <br>cd ~/documents/NGS/NGS_short_sequence/downloaded-data<br></pre>

#### Command 6: <pre>*bash* <br>mkdir SRR<br></pre>

#### Command 5: <pre>*bash* <br>cd SRR<br></pre>

## Command 23: <pre>*bash* <br>fasterq-dump SRR35879980<br></pre>
**Purpose:** When I have the accession number (like SRR35879980) of the desired read, this code downloads that fastq file for me. Fast!  
**My output:** spots read      : 18,397
reads read      : 36,794
reads written   : 36,794

## Command 24: <pre>*bash* <br>head -n 8 SRR35879980_1.fastq<br></pre>
**Purpose:** Shows the first 8 lines of the SRR35879980_1.fastq file.  
**My output:** @SRR35879980.1 VH00954:7:AAF2YK7M5:1:1101:19879:1625 length=51
CTGACATTGGCATGTTGATTTTGCCATTTTGACTATACATGGAGATGACTT
+SRR35879980.1 VH00954:7:AAF2YK7M5:1:1101:19879:1625 length=51
CCCCC;CCCCCC;CCCCCCCCCCCCCCCCCC;CCCCCCCCCCCC-CC;CCC
@SRR35879980.2 VH00954:7:AAF2YK7M5:1:1101:28267:1947 length=51
GCCCCCACACTGTGTCTGTGGTTATACTCTCTAAACATTTCAGTCACAAGC
+SRR35879980.2 VH00954:7:AAF2YK7M5:1:1101:28267:1947 length=51
CCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCC

## Command 25: <pre>*bash* <br>tail -n 8 SRR35879980_1.fastq<br></pre>
**Purpose:** Shows the last 8 lines of the SRR35879980_1.fastq file.  
**My output:** @SRR35879980.18396 VH00954:7:AAF2YK7M5:1:2611:45707:55845 length=51
CGGGGCATTGATGGATCCCGCATTAGTGGAAGCGAGAACAAATGGTGATGT
+SRR35879980.18396 VH00954:7:AAF2YK7M5:1:2611:45707:55845 length=51
CCCCCCCCCCCCCCCCCCCCCC;CCCCCCCCCCCCCCCCCCCCCCCCCCCC
@SRR35879980.18397 VH00954:7:AAF2YK7M5:1:2611:35576:55940 length=50
CACGTGCCTGAAGTACAGAGAACCCATGTTGTTCAAGGTAGTGTAACCAT
+SRR35879980.18397 VH00954:7:AAF2YK7M5:1:2611:35576:55940 length=50
CCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCC

## Command 26: <pre>*bash* <br>expr $(wc -l < SRR35879980_1.fastq) / 4<br></pre>
**Purpose:** This is an interesting command. Two embeded. 'expr' runs simple arithmetic or text. 'wc -l' counts the lines in the file given.   
**My output:** 18397 - both SRR35879980_1.fastq and SRR35879980_2.fastq have the same number of reads.

## Command 26: <pre>*bash* <br>for f in *.fastq; do; echo "$f has $(expr $(wc -l < $f) / 4) reads."; done<br></pre>
**Purpose:** This loop counts the number of reads in all of the files in the directory.    
**My output:** SRR35879980_1.fastq has 18397 reads.
SRR35879980_2.fastq has 18397 reads.

#### Command 5: <pre>*bash* <br>cd /Users/mahoo/documents/NGS/NGS_short_sequence/downloaded-data<br></pre>

#### Command 6: <pre>*bash* <br>mkdir FastQC<br></pre>

#### Command 5: <pre>*bash* <br>cd FastQC<br></pre>

## Command 27: <pre>*bash* <br>conda --version<br></pre>
**Purpose:** I wanna make sure I have conda installed. 
**My output:** conda 25.7.0

## Command 28: <pre>*bash* <br>conda install -c bioconda fastqc<br></pre>
**Purpose:** Installs fastqc through conda.
**My output:** I'm missing Java, so I have to run another code downloading Java to use fastqc.

## Command 28: <pre>*bash* <br>conda install -c conda-forge openjdk<br></pre>
**Purpose:** Installs Java.
**My output:**






