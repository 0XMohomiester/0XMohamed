## Hello! I'm [Mohamed](https://twitter.com/0xMohomiester) This is My Writeup for [Encryption - Crypto 101](https://tryhackme.com/room/encryptioncrypto101) TryHackme Room Let's start with:

Task 1) I am ready to learn about encryption  

No Answer Needed  

Task 2)  

1) I agree not to complain too much about how theory heavy this room is. 

No Answer Needed 

2) Are SSH keys protected with a passphrase or a password? 

Answer is `Passphrase` -  why `Passphrase` ? by asking to google: 
Passphrase - Separate to the key, a passphrase is similar to a password and used to protect a key.  

Task 3) Why Encryption is Important?  

Cryptography is used to protect confidentiality, ensure integrity, ensure authenticity. You use cryptography every day most likely, and you’re almost certainly reading this now over an encrypted connection.  

1) What does SSH stand for?  

Answer is `Secure Shell` 

2) How do webservers prove their identity? 

Answer is `certificates` 

3) What is the main set of standards you need to comply with if you store or process payment card 
details?

Answer is `PCI-DSS` - by asking google: 

The Payment Card Industry Data Security Standard is an information security standard for organizations that handle branded credit cards from the major card schemes. The PCI Standard is 
mandated by the card brands but administered by the Payment Card Industry Security Standards Council. 

Task4) crusial crypto maths 

1) What's 30 % 5? 

Answer is `0` 

2) What's 25 % 7

Answer is `4` 

3) What's 118613842 % 9091?

Answer is `3565` 

Task 5) Types of Encryptions

1) Should you trust DES? Yea/Nay –

Answer is `Nay`  

Symmetric encryption are DES (Broken) and AES. These algorithms tend to be faster than asymmetric cryptography and use smaller keys (128- or 256-bit keys are common for AES, DES keys are 56 bits long). 

2) What was the result of the attempt to make DES more secure so that it could be used for longer?

Answer is `Triple DES` 

3) Is it ok to share your public key? Yea/Nay

Yea - Because public key encrypt data only not decrypt 

Task 6) RSA – Rivest shamir Adleman 

1)  p = 4391, q = 6659. What is n? 

Answer is `29239669` - just like the image below :

![Screen Shot 2021-06-10 at 6 46 37 PM](https://user-images.githubusercontent.com/47929033/124304082-85533480-db63-11eb-8fad-4a7e50c2a260.png)

2) I understand enough about RSA to move on, and I know where to look to learn more if I want to. - 

No Answer is needed 

Task 7) Establishing keys Using Asymmetric Cryptography 

1) I understand how keys can be established using Public Key (asymmetric) cryptography. 

No Answer Needed 

Task 8) Digital Signatures and Certificates 

1) What company is TryHackMe's certificate issued to? 

Answer is `Cloudflare` -  Just Like the Photo Below : 

![cert](https://user-images.githubusercontent.com/47929033/124304580-2e019400-db64-11eb-8b7d-cf90acca62d6.png)

Task 9) SSH Authentication

1) I recommend giving this a go yourself. Deploy a VM, like Linux Fundamentals 2 and try to add an SSH key and log in with the private key  

No Answer Needed 

2) Download the SSH Private Key attached to this room 

No Answer Needed 

3) What algorithm does the key use? 

Answer is `RSA`-  Just Like the image Below :

![Screenshot_2021-06-10_13_11_14](https://user-images.githubusercontent.com/47929033/124304935-aec09000-db64-11eb-8bd4-49237e09151f.png)

After copying the RSA private key to new file :  

![Screenshot_2021-06-10_13_11_51](https://user-images.githubusercontent.com/47929033/124305069-e2031f00-db64-11eb-8e26-cfb21c64dc91.png)

![Screenshot_2021-06-10_13_14_01](https://user-images.githubusercontent.com/47929033/124305148-fc3cfd00-db64-11eb-8744-7ebc56f41d32.png)
 
As you see I used ssh2john to extract hash to crack it with johntheripper

4) Crack the password with John the Ripper and rockyou, what's the passphrase for the key?

Answer is `delicious` -  just like the image below : 

![Screenshot_2021-06-10_13_17_56](https://user-images.githubusercontent.com/47929033/124305481-71a8cd80-db65-11eb-9f96-5a166dad1703.png)

Task 10) Explaining Difile Hellman key exchange 

No Answer Needed

Task 11) PGP, GPG, AES 

1) Time to try some GPG. Download the archive attached and extract it somewhere sensible. 
No Answer Needed 

2) You have the private key, and a file encrypted with the public key. Decrypt the file. What's the secret word?  

Answer is Pineapple  … Just Like The Photo Below :

![Screenshot_2021-06-11_15_08_45](https://user-images.githubusercontent.com/47929033/124305814-dd8b3600-db65-11eb-99be-f7ddf6b1b3c5.png)

Task 12) I understand that quantum computers affect the future of encryption. I know where to look if I want to learn more. 

No Answer Needed  
 

 









