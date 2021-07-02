### Hello!! 
#### This is my writeup for FurtherNmap Room THM
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
###### Answer is –p 1000-1500 (by using command (nmap –h ) can show PORT SPECIFICATION AND SCAN ORDER)
###### 14) How would you tell nmap to scan all ports? 
###### Answer is –p- (by using command (nmap –h ) can show PORT SPECIFICATION AND SCAN ORDER)
###### 15) How would you activate a script from the nmap scripting library (lots more on this later!? 
###### Answer is –scripts (by using command (nmap –h ) can show scripts scan)
###### 16) How would you activate all of the scripts in the "vuln" category?
###### Answer is -–script=vuln (by using command (nmap –h ) can show scrips scan) 
###### --script=<Lua scripts>
###### Task 4 ) scan types  Overview 
###### In this task THM show me scan types and techniques three basics scan types:
###### 1) TCP connect scan (-sT)
###### 2) SYN “half-open” scan (-sS)
###### 3) UDP scan (-sU)
###### Another scan types:
###### 1) TCP Null Scans
###### 2) TCP FIN Scans
###### 3) TCP Xmas Scans 
###### No answer needed. 
###### Task 5) Tcp Connect Scan 
###### In this task I learned how devices and computer communicate with each other over the network and how to monitor network traffic with wireshark and understand what is 
###### 3-way-handshake … 
###### 1) Which RFC defines the appropriate behaviour for the TCP protocol? 
###### Answer is RFC 793     which. An RFC standard for (request for comment) based on TCP 
###### 2) If a port is closed, which flag should the server send back to indicate this? 
###### Answer is RCT   which means to reset flag because port is closed on target machine 

###### Task 6)  SYN SCAN 
###### In this task I learned some techniques about scan types just like syn scan which attacker send syn flag packet to target machine to scan open port if port is open target machine responded to attacker with (syn/ack) flag which acknowledge with connection Then attacker terminate the connection with RST flag which means to:
###### (Half-open scan or stealth scan) 

###### 1) There are two other names for a SYN scan, what are they? 
###### Answer is Half-open scans or Stealth scans.  why? Because it depends on two operation --> (syn flag, syn/ack) doesn't complete  3-way-handshake
###### 2) Can Nmap use a SYN scan without Sudo permissions (Y/N)? 
###### Answer is N 

###### Task 7) UDP SCAN 
###### 1) If a UDP port doesn't respond to an Nmap scan, what will it be marked as? 
###### Answer is open/filtered 
###### 2) When a UDP port is closed, by convention the target should send back a "port unreachable" message. Which protocol would it use to do so? 
###### Answer is icmp   which icmp 

###### Task 8) NULL, FIN, XMAS 
###### In this task I learned another techniques about scan types which are null fin xmas lest start with first question 
###### 1) Which of the three shown scan types uses the URG flag?

###### Answer is xmas    which xmas send (PSH, URG and FIN)  flags to client and if port is closed client respond with RST flag 
![ABCxAwf](https://user-images.githubusercontent.com/47929033/124309351-dfa3c380-db6a-11eb-9f12-63c03520b5e9.png)

###### 2) Why are NULL, FIN and Xmas scans generally used? 
###### Answer is Firewall Evasion ….   Many firewalls are configured to drop incoming TCP packets to blocked ports which have the SYN flag set by sending requests which do not contain the SYN flag we effectively bypass this kind of firewall  
###### 3) Which common OS may respond to a NULL, FIN or Xmas scan with a RST for every port? 
###### Answer is Microsoft Windows   in Microsoft Windows are known to respond with a RST to any malformed TCP packet regardless of whether the port is open or not. This results in all ports showing up as being closed. 
###### Task 9) ICMP Network Scanning 
###### 1) How would you perform a ping sweep on the 172.16.x.x network (Netmask: 255.255.0.0) using Nmap? (CIDR notation) 
###### Answer is nmap –sn 172.16.0.0/16 this type of scan called ping sweep. Which client send icmp packet to each possible ip address on the network  

###### Task 10) NSE overview
###### In this task I learned what is NSE?  and how to use? And why I need it?  NSE is standard for Nmap Scripting Engine thar user in vulnerability scanning and is written in lua programming language which contain some category just like: intrusive, vuln, exploit 
###### 1) What language are NSE scripts written in? 
###### Answer is Lua 
###### 2) Which category of scripts would be a very bad idea to run in a production environment?  
###### Answer is intrusive

###### Task 11) Working with NSE 
###### If we need to use NSE we can use he following command :
###### Nmap –script=<script name> 
###### 1) What optional argument can the ftp-anon.nse script take? 
###### Answer is maxlist   we can go to directory which Nmap saved scripts: /usr/share/nmap/scripts 
###### Just like the Photo Below : 







 
