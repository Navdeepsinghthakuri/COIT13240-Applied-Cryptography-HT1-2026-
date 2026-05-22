Weelk 7:
Task 1: TLS 1.2 with Diffie-Hellman Capture Analysis

Q1: Draw a message sequence diagram showing the TLS messages.
 
 <img width="272" height="203" alt="image" src="https://github.com/user-attachments/assets/6e1c97ec-3c5d-492c-b994-7f4aa7e6e2ef" />


 
Q2: Identify which TLS messages are encrypted and which are not.
 Encrypted vs Unencrypted Messages
•	Unencrypted:
o	ClientHello
o	ServerHello
o	Certificate
o	ServerKeyExchange
o	ServerHelloDone
o	ClientKeyExchange
o	ChangeCipherSpec
•	Encrypted:
o	Encrypted Handshake Messages (Finished)
o	Encrypted Application Data

Q3: What size DH key (prime, p) is used?
Identify which TLS messages are encrypted and which are not.

<img width="243" height="198" alt="image" src="https://github.com/user-attachments/assets/47d67fe0-aedd-4924-92ea-5571232b1880" />

 
The Diffie-Hellman key (prime p) in this TLS 1.2 connection is 2048 bits long (256 bytes × 8 bits = 2048 bits). This is confirmed by the Diffie-Hellman Parameters portion of the ServerKeyExchange message, which specifies the p field length as 256 bytes.

Q4: What DH key sizes is the client willing to use?

<img width="182" height="148" alt="image" src="https://github.com/user-attachments/assets/27309daf-53ad-4187-8abb-d468b7b8da35" />

The ClientHello message indicates that the client supports the following Diffie-Hellman key sizes: ffdhe2048 and ffdhe3072, which correspond to 2048-bit and 3072-bit finite field DH keys, respectively. This may be observed in the Supported Groups extension of the Client Hello packet.

Q5: What size RSA key is used in the certificate?

 <img width="213" height="174" alt="image" src="https://github.com/user-attachments/assets/e8924b76-d345-4080-a35b-de6ae7d20a30" />

The server's certificate has an RSA key with a modulus of 2048 bits. This is shown in the Subject Public Key Info portion of the Certificate message, with a modulus of 256 bytes (256 × 8 = 2048 bits).

Q6: If the round-trip-time (RTT) between web browser and web server is 50 ms, what is the delay from when a user clicks an HTTPS link until the first web page is received?
Ans:  If the round-trip time (RTT) between the web browser and web server is 50 milliseconds, it will take around 150 milliseconds for a user to click on an HTTPS link and see the first page. This is because the TLS 1.2 handshake utilising Diffie-Hellman needs around three round trips to exchange encrypted application data.

Task 2: apture Analysis
Q1: Draw a message sequence diagram of the TLS 1.3 handshake.

 <img width="204" height="237" alt="image" src="https://github.com/user-attachments/assets/b30e4603-3ce0-4295-8dc4-14efc81fc1c1" />

Q2: Which TLS 1.3 messages are encrypted, and which are not?

Unencrypted (plaintext):
•	ClientHello
•	ServerHello
Encrypted:
•	EncryptedExtensions
•	Certificate
•	CertificateVerify
•	Finished
•	All Application Data (e.g., GET, HTTP/1.1 200 OK)
•	NewSessionTicket
•	Alert(CloseNotify)

Q3: What cipher suite is used in the TLS 1.3 session?

 <img width="324" height="264" alt="image" src="https://github.com/user-attachments/assets/1c7c6f02-d6f4-4073-83fc-3a7984953da6" />


The cipher suite used is TLS_AES_128_GCM_SHA256.
Q4: 4: How does the cipher suite and protocol exchange differ from TLS 1.2 with DH?
Ans: TLS 1.3 offers some improvements over TLS 1.2 using Diffie-Hellman. While TLS 1.2 transmits most handshake messages in plaintext, TLS 1.3 encrypts all handshake messages after ServerHello. Another simpler and safer cypher suite structure used by TLS 1.3 is AEAD (Authenticated Encryption with Associated Data), which combines encryption with authentication. The handshake for TLS 1.3 is often faster than that of TLS 1.2, needing just one round-trip (RTT) instead of two or three. Additionally, because TLS 1.3 does not allow older techniques like RSA key exchange, CBC mode, or static DH, it is inherently more secure.
Q5:
	By reducing the number of round trips needed for the handshake, TLS 1.3 outperforms TLS 1.2 with Diffie-Hellman. While TLS 1.2 typically needs three round trips, resulting in a delay of around 150 ms with a 50 ms RTT, TLS 1.3 completes the handshake in a single round trip, reducing the latency to about 50 ms. This improvement significantly increases connection speed and responsiveness.

Task 3: Connecting the vm

<img width="266" height="272" alt="image" src="https://github.com/user-attachments/assets/10a6e366-df31-4350-a1c7-d3b9f8d9f02f" />

 <img width="204" height="220" alt="image" src="https://github.com/user-attachments/assets/a64d3626-4819-49fe-bb99-f354d4721094" />

 

Two Linux virtual machines were configured in VirtualBox utilising an internal network to test TCP communication using Netcat. Each virtual machine (VM) was assigned a static IP address: 192.168.10.1 for the server and 192.168.10.2 for the client. After a successful ping from the client to the server verified connectivity, Netcat was used to listen on port 12345 on the server. The client virtual machine sent a test message after establishing a connection with the server's IP address. When the message was successfully received on the server virtual machine, it was verified that TCP communication between the virtual machines was operating as intended. This challenge demonstrated practical networking abilities in a virtualized environment using basic technologies like Netcat. 

Tutorial 7 Reflection:
I gained an improved understanding of how TLS protocols operate in practical scenarios by using Wireshark to examine packet captures of TLS 1.2 and 1.3. I learned how to interpret real network data and how different versions of encryption and handshake protocols differ. My practical abilities in IP address setting, connection testing, and virtual network troubleshooting were also improved by the Netcat-based VM networking assignment. This training has improved both my academic understanding and my hands-on experience with secure communication and system configuration.
