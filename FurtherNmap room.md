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

###### 4) Nmap provides a switch to detect the version of the services running on the target. What is this switch?
###### Answer is  -sV  (by using command (nmap –h ) can show versions and services detection) 
###### 5) The default output provided by nmap often does not provide enough information for a pentester. How would you increase the verbosity?
###### Answer is –v  (by using command (nmap –h ) can show OUTPUT section) 
###### 6) Verbosity level one is good, but verbosity level two is better! How would you set the verbosity level to two? (Note: it's highly advisable to always use at least this option)
###### Answer is –vv (showing more output by adding v  --> verbosity) 
###### 7) What switch would you use to save the nmap results in three major formats? 
###### Answer is –oA  (by using command (nmap –h ) can show OUTPUT section)
###### -oA --> Output in the three major formats at once
###### 8) What switch would you use to save the nmap results in a "normal" format? 
###### Answer is –oN  (by using command (nmap –h ) can show OUTPUT section) 
###### 9) A very useful output format: how would you save results in a "grepable" format? 
###### Answer is –oG (by using command (nmap –h ) can show OUTPUT section) 
###### 10) Sometimes the results we're getting just aren't enough. If we don't care about how loud we are, we can enable "aggressive" mode. This is a shorthand switch that activates service detection, operating system detection, a traceroute and common script scanning.   How would you activate this setting? 
###### Answer is –A   …  by adding  the -A flag on your Nmap command, you can discover the operating system information of the hosts that are mapped. The -A flag can be used in combination with other Nmap commands. Using the -O flag on your Nmap command will reveal further operating system information of the mapped hosts
###### 11) Nmap offers five levels of "timing" template. These are essentially used to increase the speed your scan runs at. Be careful though: higher speeds are noisier, and can incur errors!   How would you set the timing template to level 5? 
###### Answer is –T5  (by using command (nmap –h ) can show TIMING AND PERFORMANCE)
###### 12) We can also choose which port(s) to scan How would you tell nmap to only scan port 80?
###### Answer is –p 80 (by using command (nmap –h ) can show PORT SPECIFICATION AND SCAN ORDER)
###### 13) How would you tell nmap to scan ports 1000-1500?


 
