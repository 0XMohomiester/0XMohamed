### Hello!! 
###### This is my writeup for FurtherNmap Room THM
###### Lest start with : 
###### Task 1 ) DEPLOY --- No Answer Needed
###### I need to deploy the machine to access it and connect to THM VPN NETWORK Using OpenVPN to answer the question 
###### Task 2 )  introduction 
###### In this task he talks to me about Nmap and what is Nmap  and how can I use it to find open ports on target machine and how machines working together (understand interworking) 
###### 1) What networking constructs are used to direct traffic to the right application on a server?
###### Answer is Ports 
###### Port is a Number to uniquely identify a transaction over the Network by specifying between hosts on Network 
###### 2) How many of these are available on any network-enabled computer? 
###### Answer)65535  
###### Every computer has a total of 65535 available Ports 
###### 3) [Research] How many of these are considered "well-known"? (These are the "standard" numbers mentioned in the task) 
###### Answer is 1024 
###### By asking google I found that the Ports Between UDP and TCP are 65535 Ports available for communication between devices and this impressive are three classes of port: 1 Well-known ports: Range from 0–1023. 

###### Task 3) Nmap switches  
###### 1) What is the first switch listed in the help menu for a 'Syn Scan' (more on this later!)? 
###### Answer is  –sS  (by using command (nmap –h ) can show scan techniques)
###### 2) Which switch would you use for a "UDP scan"? 
###### Answer is –sU  (by using command (nmap –h ) can show scan techniques)
###### 3) If you wanted to detect which operating system the target is running on, which switch would you use? 
###### Answer is  –O (by using command (nmap –h ) can show OS detection)

 
