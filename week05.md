Week 5:
1.	RSA Key Generation
a.	Randomly choose two different primes that are greater 175 and less than 410

	The two distinct prime numbers that we selected are q = 199 and p = 389.

 <img width="453" height="108" alt="image" src="https://github.com/user-attachments/assets/c30688d0-79a6-4123-a351-4059cd646ceb" />
 

b.	Generate your own RSA key pair (using the primes you chose).
	The generated RSA key pair are : private key : e= 5, n = 77411
Public  key : d= 15365, n = 77411

<img width="452" height="53" alt="image" src="https://github.com/user-attachments/assets/4845be05-032b-4975-a771-fd14433f02c2" />

 
 

c.	Share your public key with others in the class by posting the key on Teams :
	I gave a friend Roman access to my key. We received the  

<img width="452" height="96" alt="image" src="https://github.com/user-attachments/assets/65845335-daa6-43a0-91ce-6aa1a4605f61" />


2
a.	 I chose a three-digit message at random: M = 121
b. I used c = pow(m, e, n) in Python to encrypt the message using my own public key (e = 5, n = 77411), and the resultant encrypted message is c = 56628. This indicates that message 321 is encrypted in ciphertext C = 56628. 

 <img width="442" height="100" alt="image" src="https://github.com/user-attachments/assets/05391a20-16bc-4c26-b90a-cc2ccd857783" />



C: I sent my friend Roman this encrypted message in the following format:

<img width="458" height="152" alt="image" src="https://github.com/user-attachments/assets/90ae0bde-0039-4bf7-bd7f-7cf7ac13409f" />

 

D: Roman used his private key to decode the interaction and verified that the plaintext matched the original.

<img width="283" height="152" alt="image" src="https://github.com/user-attachments/assets/350f3f45-2328-43cc-b9dd-3ac83d0acde0" />

 
Q3: . RSA Keys in OpenSSL

<img width="283" height="184" alt="image" src="https://github.com/user-attachments/assets/ac339770-8fb3-492b-82db-e6c4ccb2577d" />

 
I used OpenSSL to create a 2048-bit RSA key pair. The public key was stored as navdeep_public.pem and the private key as navdeep_private.pem. The modulus and public exponent, e = 65537, were displayed when I viewed the public key information using openssl rsa -text. This verified that the key was produced accurately and was prepared for sharing.

Q4: . RSA Encryption in OpenSSL

 <img width="452" height="84" alt="image" src="https://github.com/user-attachments/assets/27b44ab5-cbeb-496e-8ab9-414e7ed39b26" />
 

I used OpenSSL to encrypt a message using my RSA public key and decode it with my private key. Since rsautl has been deprecated, I used pkeyutl. The message "This is a secret message for Roman." was successfully encrypted and then converted back to plain text. This verified that OpenSSL and RSA encryption and decoding operate safely.

Reflection:
This week, I used OpenSSL and manual processes to generate RSA key pairs as part of my investigation into public-key cryptography. I worked on using RSA techniques to encrypt and decrypt communications and trading ciphertext with peers. Additionally, I studied the structure of RSA keys stored in PEM files and learnt how to manage private and public keys securely. My understanding of asymmetric encryption and its practical applications for secrecy and safe communication has improved. 

