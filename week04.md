
Week 4
Q1: Exclusive OR



Bit Position	A	B	A ⊕ B
1	            0	1	1
2	            1	1	0
3	           0	1	1
4	           1	0	1
5	           0	0	0
6	           0	1	1

Final Result:
A	      B	    A ⊕ B
010100	111001	101101
010100 ⊕ 111001 = 101101


Q2: Simple Block Cipher (SBC) [10 min]
Task:

Encrypt a random 5-bit plaintext using SBC with a 3-bit key
Decrypt the ciphertext 11111 using a random 3-bit key.
From SBC lookup table from:

	An example of encryption Suppose:
	01010 is the plaintext.
	110 → is the key. Look up column 110 and row 01010.

	for an example of decryption:
	11111 is the ciphertext.
	Key = 101 by  Locating  the matching row (plaintext) for 11111 in column 101.


Q3: SBC in CBC Mode
TASK:
•	Choose.              random values:
A =                      10101
B =                       01110
→ P1 = ABA = 101010111010101
•	Key K1 = 110
•	IV1 = 10011
CBC Encryption Steps:
1.	Split P1 into 3 blocks: 10101, 01110, 10101
2.	CBC process:
o	C0 = IV1
o	C1 = SBC(K1, P1_1 ⊕ C0)
o	C2 = SBC(K1, P1_2 ⊕ C1)
o	C3 = SBC(K1, P1_3 ⊕ C2)
Q4: SBC in CTR Mode [20 min]
task:
•	Use same P1, K1, and IV1
CTR mode:
•	Use IV1 as counter, incremented each block
•	Encrypt counter with SBC, then XOR with plaintext block:
o	C1 = P1_1 ⊕ SBC(K1, CTR1)
o	C2 = P1_2 ⊕ SBC(K1, CTR2)
o	C3 = P1_3 ⊕ SBC(K1, CTR3)
CTR1 = IV1, CTR2 = IV1+1, etc.

Q5: Compare Modes of Operation.
Mode 	Description 	Pros 	cons
ECB	encrypts every block separately	Easy and quick.	The ciphertext is not secure when identical blocks are used.
CBC	Each block is XORed with the ciphertext that came before it.	conceals patterns, making it safer.	slower and requires an IV
			
CTR	XORs the output with plaintext and uses the counter as input to block the cypher	Fast and parallelizable.	needs special counters and cautious application.


 



Q6: Encryption in Python
 
Ans: For this project, I used Python's cryptography library to build AES encryption and decoding. By successfully encrypting the message "Hello Cryptography!" and then decrypting it back to its original format, the script confirmed that the process was proper. This exercise helped me better grasp the actual applications of symmetric encryption, especially how keys and initialisation vectors (IVs) are utilised to enable safe data encryption.
Reflection: 
This week, I completed practical tasks that showed me how block cyphers work using Python and a simple block cypher (SBC).  By practicing encryption and decryption using XOR and several modes including ECB, CBC, and CTR, I was able to better comprehend how data security varies between modes.  I also created AES encryption in Python using the cryptography package, accurately confirming encryption and decryption.  All things considered, the exercises improved my understanding of symmetric encryption and its applications.
