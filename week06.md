Week 6:
Task 1: Manual DHKE
Task 1: Perform the DHKE with your partner, sending messages in Teams.
<img width="451" height="231" alt="image" src="https://github.com/user-attachments/assets/865f5a92-9897-403e-9e16-e4329863b6a3" />

 
I verified with him that we had the same secret. 
I completed the Diffie-Hellman Key Exchange (DHKE) with Roman using the established values: prime p = 31 and generator g = 12. I selected my private key, a = 15, to retrieve my public key, P U = 25. Roman's public key is P U = 16. As the shared secret Mod31, I came up with 16^15 m od. Roman confirmed that he too obtained the result 1 when I asked him to compute the shared secret using both his private key and mine. This confirmed the efficacy of the DHKE. This experiment has helped me better grasp how two parties may safely generate a shared key over an unsecured channel without revealing their private values.


1.	Confirm with your partner that the DHKE was successful, i.e., check you both obtained the same secret.

Roman’s output 

<img width="368" height="263" alt="image" src="https://github.com/user-attachments/assets/9c88614b-152a-4aa1-99e7-7d9e5a4598a2" />

Roman and I verified that we received the same code.

2.	Identify all the values from the DHKE that are private to you, and all the values that are public.
   
   <img width="262" height="137" alt="image" src="https://github.com/user-attachments/assets/9fae8f2d-9532-41a9-8eb8-1ead91b2a12c" />

 
Task 2: DHKE in OpenSSL
Q2: : Create your own DH public and private key. 

<img width="249" height="282" alt="image" src="https://github.com/user-attachments/assets/580f2d78-eec1-4974-9009-40d7f6c0b5f7" />


1.	Share the parameters and public key with partner.
   
   <img width="178" height="202" alt="image" src="https://github.com/user-attachments/assets/2bded2c4-9e02-4b78-9ae7-5d74bd186de5" />

 
I provided the public key parameters with Roman.



4:) Generate a shared secret

<img width="297" height="188" alt="image" src="https://github.com/user-attachments/assets/b911b296-c41c-4a60-b4c8-579ebc75c0b3" />


 
Navdeep’s shared secret


<img width="268" height="185" alt="image" src="https://github.com/user-attachments/assets/767086c7-f1c3-463f-951b-a1e4af6081ad" />

 
Roman’s shared secret
I generetared the shared secret 
5: Confirm that both you and your partner have the same shared secret by visually comparing
output with xxd.

 <img width="367" height="108" alt="image" src="https://github.com/user-attachments/assets/754cfc53-faed-4aa4-9661-4f122e17540a" />

Roman’s output

<img width="282" height="131" alt="image" src="https://github.com/user-attachments/assets/ddb38a0a-98c9-428a-9734-81b5e02eef8d" />

 
Navdeep output
We verified that we obtained the same result as depicted in the image above.

Reflection: 
This week, I learned that the Diffie-Hellman Key Exchange (DHKE) allows two parties to safely create a shared secret across an unsecured channel. The DHKE is manually executed using Roman p, generator, and certain prime integers. 
We used g and our private keys to accurately compute the same shared secret. This confirmed that the key exchange process was operating correctly. The activity gave me a realistic grasp of how public and private values work together to foster safe communication. Additionally, it underlined how important authentication is since DHKE is vulnerable to man-in-the-middle attacks without it. 

