## Investigating windows
Hello! i am [mohamed](https://twitter.com/0xMohomiester) This My Writeup for Investigating windows tryhackme room Let’s Start with:

Task1) Investigating Windows 

1) What's the version and year of the windows machine?  

Answer is `windows server 2016 – by using` by using command `systeminfo` on cmd  Just Like the photo 
below:

![Screen Shot 2021-06-16 at 8 31 18 PM](https://user-images.githubusercontent.com/47929033/125171741-063eab80-e1b6-11eb-98e9-4020a5354955.png)

2) Which user logged in last?

Answer is `Administrator` – Because I am in directory: “C:\Users\Administrator>”

3) When did John log onto the system last? Answer format: MM/DD/YYYY H:MM:SS AM/PM  

Answer is `03/02/2019 5:48:32 PM` – By using command `net user John`  Just like the photo Below: 

![Picture1](https://user-images.githubusercontent.com/47929033/125171863-df34a980-e1b6-11eb-8b36-3f0f654cd195.png)
 
4) What IP does the system connect to when it first starts? 

 Answer is `10.34.2.3` -- Just like the Photo below:

![Screen Shot 2021-06-16 at 8 29 52 PM](https://user-images.githubusercontent.com/47929033/
125171888-fa9fb480-e1b6-11eb-9347-db668d5ce514.png)
 
5) What two accounts had administrative privileges (other than the Administrator user)? 

Answer format: username1, username2 

Answer is Jenny, Guest – first check for user on the system by command: `net user`

![Screen Shot 2021-06-16 at 8 41 53 PM](https://user-images.githubusercontent.com/47929033/125171927-2327ae80-e1b7-11eb-89f1-7ec5f664994d.png)
 
by checking users privilege Using command: `net user Guest` for Guest user, and `net user Jenny` for 

Jenny user ... Just Like the photo below : 

![Screen Shot 2021-06-16 at 8 42 22 PM](https://user-images.githubusercontent.com/47929033/125171965-46eaf480-e1b7-11eb-8adc-ca94ea19b12c.png)

![Screen Shot 2021-06-16 at 8 42 43 PM](https://user-images.githubusercontent.com/47929033/125171978-566a3d80-e1b7-11eb-8718-d55ebc8cca94.png)

 6) What's the name of the scheduled task that is malicious? 
 
 Answer is clean file system … open scheduled task Just like the photo below:

![Screen Shot 2021-06-14 at 1 59 31 AM](https://user-images.githubusercontent.com/47929033/125172026-8fa2ad80-e1b7-11eb-927c-55bab6bc1676.png)

Open Task Schedular Library and got to `clean the system` and see the Action tab that command used 
 

netcat to listening on port 1348 ... it’s malicious 

7) What file was the task trying to run daily? 

Answer is `nc.psi` 

8) What port did this file listen locally for? 

Answer is `1348` 

9) When did Jenny last logon? 

Answer is `Never`.. using command: `net user Jenny` Just like the photo below to see the last logon: 

![Screen Shot 2021-06-16 at 8 42 43 PM](https://user-images.githubusercontent.com/47929033/125172089-dc868400-e1b7-11eb-95f6-b307518afbd7.png)

 10) At what date did the compromise take place? 
 Answer format: MM/DD/YYYY 
 Answer is 03/02/2019 By opening Task schedular and go to Gameover Task and see The Action tab … we find: 

![Screen Shot 2021-06-16 at 9 07 20 PM](https://user-images.githubusercontent.com/47929033/125172119-00e26080-e1b8-11eb-83eb-2699f2181656.png)

 That a program called “mimi.exe” stored in TMP directory and it start every 5 minutes 
 And redirect to save the output in o.txt in the same directory... the content of file:

![Screen Shot 2021-06-16 at 9 20 26 PM](https://user-images.githubusercontent.com/47929033/125172157-5454ae80-e1b8-11eb-8150-cd228327be75.png)

 As you can see which used tool called `mimkatz` is used for capturing windows password 
 11) At what time did Windows first assign special privileges to a new logon? 
 Answer format: MM/DD/YYYY HH:MM:SS AM/PM 
 Answer is 03/02/2019 4:04:49 PM... by opening event viewer and go to windows logs and to security tab and scroll down to see 03/02/2019 … Just like the Photo Below: 

![Screen Shot 2021-06-14 at 7 45 19 PM](https://user-images.githubusercontent.com/47929033/125172191-91b93c00-e1b8-11eb-90a1-928d3368ecc9.png)

 12) What tool was used to get Windows passwords? 
 Answer is Mimikatz 
 13) What was the attackers external control and command servers IP? 
 Answer is 76.32.97.132 … By asking google I find that the windows host file used for maps the server and hostnames and ip addresses that stored in “C:\Windows\system32\drivers\etc\hosts … content of hosts file: 

![Screen Shot 2021-06-14 at 7 20 51 PM](https://user-images.githubusercontent.com/47929033/125172236-cfb66000-e1b8-11eb-93fb-01a6e0882006.png)

 14) What was the extension name of the shell uploaded via the servers website? 
 Answer is .jsp  … by asking google I find Microsoft uses IIs (internet information services) 
 As a default web browser on the windows. and inetpub is the default folder situated under “C:\Inetpub”.... we can go to the directory and go to “wwwroot” is a folder it contains a  webserver content … Just Like the photo Below: 

![Screen Shot 2021-06-14 at 7 28 05 PM](https://user-images.githubusercontent.com/47929033/125172256-ed83c500-e1b8-11eb-9dce-c8ec5f8ce713.png)

 15) What was the last port the attacker opened? 
 Answer is 1337 … by opening firewall inbound role and see the rules: 

![Screen Shot 2021-06-14 at 7 24 17 PM](https://user-images.githubusercontent.com/47929033/125172285-1dcb6380-e1b9-11eb-9efd-fbd427f06021.png)

 16) Check for DNS poisoning, what site was tar
 Answer is google.com … we can see in the photo below: 


![Screen Shot 2021-06-14 at 7 20 51 PM](https://user-images.githubusercontent.com/47929033/125172335-7d297380-e1b9-11eb-8d0f-75e6c2727ed3.png)
















