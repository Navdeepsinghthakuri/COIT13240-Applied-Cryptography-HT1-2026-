
Week 8
Q1: Copy Example Python Code

Step 1: Download Example Files from Unit GitHub Repo

 <img width="452" height="246" alt="image" src="https://github.com/user-attachments/assets/891a29a2-bd9d-410a-8053-b65cfaa8f3bc" />

I downloads all the 6 give file from our team group which made myself easy to look for.

Step2: Upload Files to Your Journal Repo

<img width="344" height="182" alt="image" src="https://github.com/user-attachments/assets/ac01f4b8-bfcf-427c-83c3-83700db134dd" />

 
I uploaded all the 6 files in my journal repository.
Q2. Calculate Hash in Python

 <img width="260" height="164" alt="image" src="https://github.com/user-attachments/assets/d7862421-21e6-4960-81d1-75fc6c35cb93" />

Python's cryptography package was used to hash two different messages using SHA-256 and SHA-512. The original script (hashexample1.py) hashed "Hello world" using SHA-256, but I changed it to hash "Hello COIT13240!" using SHA-512 in hashexample2.py. Interestingly, even small changes to the algorithm or message produce wildly different hashes, demonstrating the avalanche effect, which ensures strong integrity protection.

Q3. Calculate MAC in Python 

<img width="452" height="108" alt="image" src="https://github.com/user-attachments/assets/37940c93-41b5-4227-9f97-058d57b0c979" />

For this task, hashexample1.py utilised SHA-256, whereas hashexample2.py used SHA-512. Furthermore, I changed the message. The resulting hash values were completely different, and SHA-512 produced a lengthier result. This illustrates how changing the algorithm or message affects the hash, demonstrating both high data integrity and the avalanche effect.

Q4. Use the MAC Helper Functions

 <img width="423" height="104" alt="image" src="https://github.com/user-attachments/assets/25671740-5c92-4d48-b7de-98b032befb0a" />

Plaintext code of team.

<img width="452" height="67" alt="image" src="https://github.com/user-attachments/assets/b5706438-409c-406a-8753-f11bc42152da" />

 
Navdeep output

 <img width="378" height="163" alt="image" src="https://github.com/user-attachments/assets/8d3fbb94-1d73-48ca-97f8-672ef6f353a4" />

Mac-sender nano 

I created a secure communication simulation using mac.py, mac-sender.py, and mac-receiver. py. Roman, acting as the sender, generated a MAC tag for a message, which Navdeep, the recipient, confirmed.
Sebder coe(roman):
'''
Demo of mac.py from sender's perspective
'''
 
import mac
 
# Prepare message and key
message = "Hello Buddy"
key_hex = "0123456789012345678901234567890123456789012345678901234567890123"
key = mac.hex_to_binary(key_hex)
print("Original key: " + key_hex)
 
# Calculate the tag
tag_binary = mac.tag(message, key)
print("Tx message: " + message)
 
# Convert tag to base64 so can be easily sent across network
tag_text = mac.binary_to_base64(tag_binary)
print("Tx tag: " + tag_text)
 
# Send the message and tag to other side, e.g., with email or Teams
 
print("AuthenticatedMessage{{from=Roman, to=Navdeep, message={Hello Buddy}, tag={tag.hex(N3fOUtJzRYTHNbQzM2t5qvDdpVFvUiJVBd6icYVrptQ=)}}}")
receiver code (Navdeep):
Demo of mac.py from receiver's perspective
'''
import mac

# Secret MAC key must be known by receiver
key_hex = "0123456789012345678901234567890123456789012345678901234567890123"

# message and tag received
rx_message = "Hello Buddy"
rx_tag_text = "(N3fOUtJzRYTHNbQzM2t5qvDdpVFvUiJVBd6icYVrptQ="

# Convert base64 tag back to binary
rx_tag_binary = mac.base64_to_binary(rx_tag_text)

# Verify
key = mac.hex_to_binary(key_hex)
print("Rx message: " + rx_message)
print("Rx tag: " + rx_tag_text)
print("Key: " + key_hex)
r = mac.verify(rx_message, key, rx_tag_binary)
print("Verified? " + str(r))

The sender and receiver mentioned above were modified from the original file. Ultimately, we were able to extract the output by modifying the plaintext and hash that we acquired from the sender file.

Week 08 Reflection – Hash Functions and MACs
This week, I focused on creating hashes and HMACs using Python within PuTTY. I learned how cryptographic hashes ensure data integrity and how MACs prevent tampering. The real-world sender-receiver MAC verification simulation illustrated how shared keys safeguard communication. The error handling, encoding formats, and tamper testing improved my understanding of secure message authentication.






