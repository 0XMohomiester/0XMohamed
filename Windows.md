### Hello...  This My Writeup for Investigating windows THM room Let’s Start with:
###### Task1) Investigating Windows 
###### 1) What's the version and year of the windows machine? 
###### Answer is windows server 2016 – by using “systeminfo” command on cmd  Just Like the photo below:
![Screen Shot 2021-06-16 at 8 31 18 PM](https://user-images.githubusercontent.com/47929033/125171741-063eab80-e1b6-11eb-98e9-4020a5354955.png)
###### 2) Which user logged in last?
###### Answer is Administrator – Because I am in directory: “C:\Users\Administrator>”
###### 3) When did John log onto the system last?  
###### Answer format: MM/DD/YYYY H:MM:SS AM/PM  
###### Answer is 03/02/2019 5:48:32 PM – By using command “net user John” 
###### Just like the photo Below: 
![Picture1](https://user-images.githubusercontent.com/47929033/125171863-df34a980-e1b6-11eb-8b36-3f0f654cd195.png
###### 4) What IP does the system connect to when it first starts? 
###### Answer is 10.34.2.3 -- Just like the Photo below:
![Screen Shot 2021-06-16 at 8 29 52 PM](https://user-images.githubusercontent.com/47929033/125171888-fa9fb480-e1b6-11eb-9347-db668d5ce514.png))
###### 5) What two accounts had administrative privileges (other than the Administrator user)? 
###### Answer format: username1, username2 
###### Answer is Jenny, Guest – first check for user on the system by command: “net user”
![Screen Shot 2021-06-16 at 8 41 53 PM](https://user-images.githubusercontent.com/47929033/125171927-2327ae80-e1b7-11eb-89f1-7ec5f664994d.png)
###### by checking users privilege Using command: “net user Guest” for Guest user, and “net user Jenny” for Jenny user ... Just Like the photo below : 
![Screen Shot 2021-06-16 at 8 42 22 PM](https://user-images.githubusercontent.com/47929033/125171965-46eaf480-e1b7-11eb-8adc-ca94ea19b12c.png)

![Screen Shot 2021-06-16 at 8 42 43 PM](https://user-images.githubusercontent.com/47929033/125171978-566a3d80-e1b7-11eb-8718-d55ebc8cca94.png)

###### 6) What's the name of the scheduled task that is malicious? 
###### Answer is clean file system … open scheduled task Just like the photo below:
![Screen Shot 2021-06-14 at 1 59 31 AM](https://user-images.githubusercontent.com/47929033/125172026-8fa2ad80-e1b7-11eb-927c-55bab6bc1676.png)








