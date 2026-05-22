Week 9 
 Task 1:
After looking through 1.3 and finding nothing for this week, I began looking at 1.2 in order to finish all the assignments. The TLS Web Server Certificates (TLS 1.2 Analysis) are as follows:  

Task 1:
1.	Which packet/message contains the web server’s certificate?
	Packet 4, which also includes the Certificate message, contains the web server's certificate as part of the TLS 1.2 handshake between the server and the client.

2.	Who is the subject, i.e., commonName (CN)?
	The certificate's topic (commonName) is: Sandilands.info

3.	Who is the issuer?
	The Certificate Authority (CA) issued the certificate: Let's encrypt Authority X3.

4.	Who’s public key is included in the certificate?
	The certificate contains the RSA public key of the web server sandilands.info, which is used for secure communication during the handshake process.

5.	What algorithm is used for that public key?
	Using rsaEncryption, the public key algorithm is RSA with a modulus of 2048 bits.

6.	What is the value of the public key?
->   The public key's value is a large hexadecimal modulus (2048 bits). For instance, it begins with:
b5:c0:e7:... and concludes with the following:...:d6:1c:9f
(For reporting purposes, just the first and final few bytes are usually given.)

7.	Who signed the certificate?
	The certificate was signed by:Let’s Encrypt Authority X3

8.	What algorithm(s) is used for the signature?
	The signature algorithm used is:sha256WithRSAEncryption

9. What is the other certificate in the message?
ans: The certificate message also contains an intermediate Let's Encrypt Authority X3 certificate. This helps create a chain of trust from the server's certificate to a trusted root certificate authority in the client's browser.



10. How does the web browser authenticate the web server?
Ans: To authenticate the server, the browser checks if the server certificate was issued by a trustworthy CA.
 • Verifying the certificate chain up to a trustworthy root authority.
• Confirming that the URL being accessed matches the domain name (CN) on the certificate.
• Confirming that the certificate has not been revoked or expired.
• Verifying the digital signature on the certificate using the public key of the CA.



Task 2: Crypto Mechanisms in Python
 
<img width="408" height="258" alt="image" src="https://github.com/user-attachments/assets/8f3846b4-4943-41b8-af3c-c3e485ccd757" />

	In this work, I developed four basic cryptographic methods using Python in a Linux virtual machine that was accessible through PuTTY. Plaintext was successfully encrypted by the AES encryption script using CBC mode and a 256-bit symmetric key. The RSA example successfully signed and validated a message using a generated key pair, demonstrating digital signatures and integrity. The secure key exchange was confirmed when both simulated participants in the Diffie-Hellman key exchange arrived at the same shared secret. Finally, the HMAC example showed how message authentication codes inhibit verification on altered messages, protecting against manipulation. These practical examples helped me better understand how these algorithms work at the code level and will be helpful when creating safe software in the future.

Tutorial Week 9 Reflection:

This week's lesson helped me connect theoretical encryption ideas to practical applications. In Task 1, I learned how digital certificates are used to validate a web server by using Wireshark to analyse a TLS 1.2 handshake. I learned how browsers detect certificate data including the topic, issuer, public key, and signature method and validate certificate chains to increase trust. In Task 2, I created four basic cryptographic methods in Python using PuTTY on a Linux virtual computer. These included AES encryption, HMAC for integrity, RSA digital signatures, and Diffie-Hellman key exchange. The practical coding helped me better grasp how these algorithms work at the system level and how they are applied in real-world secure communications like TLS. My confidence in evaluating encrypted communications and creating cryptography tools has increased thanks to this training. This course has boosted my confidence in analysing encrypted communications and developing cryptography tools.

