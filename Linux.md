### Hello This is My Writeup for LinuxFundmentals part 2  Let's start with: 
###### Task1)intro 
###### In this task  I learned Linux essential and basics for security penetration tester  
###### No Answer Needed   
###### Task 2) Accessing Your Linux Machine Using SSH (deploy):  
###### Now I will deploy the machine (THM MACHINE) and connect to the THM Network Using OpenVPN ..
###### Let's start with ... What is SSH?  and how Does it work?  
###### SSH is standard for (Secure shell) is a protocol between devices in an encrypted tunnel that allows machines to connect to each other over the Network (encrypted Traffic) just like this: 
![ssh](https://user-images.githubusercontent.com/47929033/124278076-17e4db00-db46-11eb-8a40-e7cc04ecb66b.png)
###### After deploying my machine, I connected to the machine using ssh with username and password using command:  ssh tryhackme@10.10.74.55   
###### Machine IP: 10.10.74.55 
###### USERNAME: tryhackme
###### Password: tryhackme
###### just like this: 
![ssh1 gpg](https://user-images.githubusercontent.com/47929033/124278466-96417d00-db46-11eb-9f93-55750807c33c.png) 
###### I've logged into the Linux Fundamentals Part 2 machine using SSH! 
###### No Answer Needed 
###### Task 3) introduction to flags and switches 
###### In this task he talks to me about how to interact with Linux files system and most used commands on Linux OS …
###### 1) Explore the manual page of the ls command 
###### No Answer Needed 
###### 2) What directional arrow key would we use to navigate down the manual page? 
###### Answer is down 
###### 3) What flag would we use to display the output in a "human-readable" way?
###### Answer is –h    from manual page of ls command: 
![ls](https://user-images.githubusercontent.com/47929033/124279076-5333d980-db47-11eb-9f82-67c5b1baf91d.png)
###### Task 4) filesystem interaction continued: 
###### 1) How would you create the file named "newnote"? 
###### Answer is touch newnote …. which touch command used to create a newfile  
###### 2) On the deployable machine, what is the file type of "unknown1" in "tryhackme's" home directory? 
###### Answer is ASCII TEXT ... by using file command which prints type of file 
###### 3) How would we move the file "myfile" to the directory "myfolder" ? 
###### Answer is mv myfile myfolder .. mv <file> <destination>
###### 4) What are the contents of this file? 
###### Answer is THM{FILESYSTEM} ... BY Using Cat Command to print content of the file 
###### 5) continue to apply your knowledge and practice the commands from this task. 
###### No Answer Needed 
###### Task 5) Permission  
###### Let's start with questions: 
###### 1) On the deployable machine, who is the owner of "important"? 
###### Answer is user2 …  just like The photo below:
![user2](https://user-images.githubusercontent.com/47929033/124280038-7f038f00-db48-11eb-880f-c37b7f317828.png)
###### 2) What would the command be to switch to the user "user2"? 
###### Answer is su user2 
###### 3) Output the contents of "important", what is the flag? 
###### Answer is THM{SU_USER2} …  just like this: 
![Picture1](https://user-images.githubusercontent.com/47929033/124280694-47e1ad80-db49-11eb-90b7-6ec55955c777.png)
###### Task 6) common directories 
###### 1) READ ME 
###### No Answer Needed 
###### 2) What is the directory path that would we expect logs to be stored in? 
###### Answer is /var/log … which var means to variable data this folder stores the data that is  written by services or applications running on system just like logs file … 
###### 3) What root directory is similar to how RAM on a computer works?  
###### Answer is /tmp   …  tmp means to temporary if the computer is restarted the data in this folder are cleared out   
###### 4) Name the home directory of the root user? 
###### Answer is /root
###### 5) Now apply your learning and navigate through these directories on the deployed Linux machine. 
###### No Answer Needed 
###### Task 7) conclusion and summaries 
###### I learned how to interact with Linux file system and common directories which I need to know  and how ssh works  and how to use it between machines over the Network …... :)











