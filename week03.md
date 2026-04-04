Week 3:
Q1:
1.  Information Known by Attacker
a. KPA (Known Plaintext Attack): The attacker knows a few plaintext-ciphertext combinations but does not know the encryption key. The goal is to identify trends or weaknesses in other ciphertexts.
b. CPA (Chosen Plaintext Attack): The attacker can choose plaintexts and retrieve encrypted versions of them. This makes it easier to understand how the encryption works and perhaps get the key.
   c. CCA (Chosen Ciphertext Attack): By choosing ciphertexts, the attacker can acquire the decrypted plaintexts. As the most potent attack type, it is commonly used to exploit weaknesses in padding or decryption processes.

Q2: Modes of Operation:
   a. Effectively Encrypt Big Data: Makes it possible to encrypt data longer than a single block.
b. Prevent Recurring Patterns in Ciphertext: This keeps ciphertexts made from blocks of identical plaintext from becoming predictable.
c. Guarantee Integrity and Confidentiality: Some choices offer both encryption and message authentication.
d. Strengthen Security Against Attacks: Randomness is incorporated to prevent attacks such as pattern recognition.
e. Improve Performance for Different Use Cases: Some modes allow parallel processing, while others are better for file encryption.

Q3: . Attack on AES-128: 
Considering that an attack is 1,000,000 times quicker than brute force: 
a. 2^128 keys = 3.4 * 10^38 seconds is the brute force time. 
b. Faster assault time: 3.4 * 10^38/1,000,00 = 3.4 * 10^32 seconds
c. A year consists of 60 * 60 * 24 * 365 = 31,536,000 seconds.
d. . Convert to years: 3.4 * 10^32/3156,000 = 1.08 * 10^26. 
With a keyspace of 2^128= 3.4 × 10^32, AES-128 makes brute force quite slow. The time drops to 3.4 × 10^32 seconds even if an assault is 1,000,000 times quicker. This is still astronomically enormous when converted to years, yielding about 1.08 × 10^26years.Therefore, it is still computationally impossible to break AES-128 in practice, even with a much quicker assault and costly equipment.
Q4: 
 
The command xxd ciphertext is displayed in the terminal window in the image.Bin is executed. This command displays the contents of a file named ciphertext in hexadecimal.bin. The result shows the file's binary contents in hexadecimal.
Q5: 
 
In the terminal window seen in the picture, the command xxd -c 8 ciphertext.bin is executed. With eight bytes per line, this programme displays the hexadecimal contents of a file named ciphertext.bin.

Q6:
 <img width="226" height="165" alt="image" src="https://github.com/user-attachments/assets/4ad3b64c-94aa-4da3-809a-ddcf991d4ea5" />

   A discussion about Key Selection
The 64-bit hexadecimal key (0123456789ABCDEF) was chosen.
Eight of the 56 bits that DES really uses for encryption are parity bits.
Brute-force attacks can be prevented by employing a strong, random key.

7:

 <img width="188" height="162" alt="image" src="https://github.com/user-attachments/assets/2750b10c-e2fd-4f5b-ac86-a1b4d3e1afe6" />

The OpenSSL AES-128-CBC speed test results are displayed in the image. Performance is greatly improved in the second test (with -evp) by using hardware AES, whereas the first test operates without hardware acceleration. Compared to software AES, hardware-accelerated AES is roughly four times faster. Data is processed more effectively with larger block sizes. This facilitates system-to-system encryption performance comparison.
Q8: 
The total encryption speed would be 500,000 AES encryptions per second if I had ten $10,000 MacBook Airs, each of which could encrypt data at a rate of 50,000 encryptions per second. AES-256's key space is 2^256. The brute force time needed would be time = 2^256/500,000 = 2.316×10^71. Ten $1,000s MacBook Airs would add up to $10,000. AES-256 cannot be broken by brute force using current technology because of its significant energy consumption, hardware limitations, and prohibitive time requirements. These are some of its primary practical restrictions.

Reflection:
I studied modern cryptography ideas, including AES, attack models, and encryption modes throughout Week 3. I discovered the reason why powerful algorithms, such as AES, are essentially unbreakable. This week enhanced my ability to think critically and deepened my understanding of practical encryption and cybersecurity.


