Week 2:
Q2:
  <img width="402" height="164" alt="image" src="https://github.com/user-attachments/assets/ffbcb494-ef04-41a4-bbef-50cca7f5c0f1" />

manually decrypted the ciphertext, pjhigpaxp. I decrypted the ciphertext “pjhigpaxp” I got the encrypted word “Australia” 
Q3:

 <img width="275" height="174" alt="image" src="https://github.com/user-attachments/assets/404031f1-3c1b-410d-a89e-9c3209a2250b" />

I used the pycipher Python programme to decrypt a message that had been encrypted using the Caesar cypher. 15 was the key, and "pjhigpaxp" was the ciphertext. Caesar(). decipher() was used to obtain the plaintext "Australia," and re-encryption was used to verify the outcome. This assignment supported the notion of symmetric encryption using code.

Q4: Caesar Decrypt without Key

 <img width="223" height="226" alt="image" src="https://github.com/user-attachments/assets/c888b01b-b93f-4e7d-86e6-9025bcff1b16" />

[decrypted word  "knuprdv"]
I tried all 26 Caesar shift options in Python to decrypt "knuprdv" without knowing the right key. Nine, or "BELGIUM," was the "backing" brought on by the correct key.
Q5: 
 <img width="276" height="149" alt="image" src="https://github.com/user-attachments/assets/ca1b635c-666b-4e80-b9d8-c6bd57fee06f" />

 To Implement Caesar Cypher in Python: I developed Python methods to manually encrypt and decode Caesar cyphers using ASCII value shifting. "Australia" was encrypted using key 15 to produce "Pjhigpaxp," which was then decoded.
6.	 Q6: Brute-force decryption of a Caesar cipher in Python by trying all 26 possible key values

 <img width="282" height="152" alt="image" src="https://github.com/user-attachments/assets/5f7bcfb1-8e76-46bf-a15e-0627a064343b" />

I tested each one of the 26 Caesar keys on "pjhigpaxp" using a Python brute-force loop. The result from Key 15 matched the right plaintext, "australia." This shows how easy it is to break Caesar cyphers using brute force.
Q7: Playfair Cipher Manual Decryption:

 <img width="274" height="188" alt="image" src="https://github.com/user-attachments/assets/1bd46d6f-bb25-41cc-9adf-c99b75d3d2f8" />

The Decrypted word = “PARALLEL”
Using a 5x5 matrix constructed from the word "programme," the Playfair cypher decrypts text by eliminating duplicates. Pairs (RP, OP, IZ, UL, IZ) are created from the ciphertext rpopizuliz. Playfair rules are used to decode each pair: same row → move left, same column → move up, rectangle → swap columns. The final plaintext is PARALLEL when the padding letters (X) are removed from the resultant text, which is PARALXLELX.




Q8: Rail Fence Decrypt

 <img width="373" height="225" alt="image" src="https://github.com/user-attachments/assets/1212a3dc-4645-4314-980d-c7c9153c4325" />
 

DECRYPTED TEXT = "Internet Applications and Technologies”
The ciphertext is arranged in three rows in a zigzag pattern using the Rail Fence cypher with key 3. After the letters are arranged in rows, they are read diagonally in a zigzag pattern. The original message is recovered as follows by recreating this pattern for the ciphertext irtngapconentehooisnapiaintecledlts: Internet Applications and Technologies
Q 9: 

 <img width="448" height="253" alt="image" src="https://github.com/user-attachments/assets/6d8f41a2-d199-4081-97b6-8e604821d12a" />
 

 
The ciphertext cieaexshxettrbxass is divided into six columns using the key 164325 in the Row/Column cypher. The columns are read row by row after being rearranged in accordance with the key sequence. The decoded plaintext is as follows after padding letters (x) are removed: "Caesar is the best” I got.
Q10: One-Time Pad Brute Force
One-Time Pad Brute Force
Given:
Hexadecimal pad (base-16)
Message length = 300 chars
Brute force speed = 10^10 keys/second 
Calculation:
keyspace = 16^300 = 2^1200
Worst-case time = 2^1200/10^10 seconds
Convert to years: 10^343.74 years
The key space of a 300-character hexadecimal one-time pad is 16^300 = 2^1200, which is quite enormous. The worst-case brute force time is 2^1200 / 10^10 seconds, or around 10^33 years, even with a strong machine checking 10¹¹ keys every second.
The One-Time Pad is said to be theoretically impenetrable when used correctly, since this is so high that brute-force assaults are nearly impossible.
Reflection: 
I focused on traditional cyphers like Caesar, Playfair, Rail Fence, and Row/Column during Week 2. I was able to comprehend both the manual and Python methods of encryption and decryption. I learnt more about security principles after seeing how vulnerable some cyphers are to brute-force assaults.



