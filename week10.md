
Week 10: 
Quantum Computing and Cryptography

Q1: A bit has two states, 0 or 1. How many states does a qubit have? What are the
states?
Ans: It is possible for a qubit to exist concurrently in a superposition of its two basic states, |0⟩ and |1⟩.

Q2: If a qubit is in the state 0.8|0⟩ + 0.6|1⟩, what happens when it is measured?
Ans: When measured, the qubit collapses to a single state. It has a 64% probability of becoming 0 and a 36% chance of becoming 1.

Q3: Quantum computing can reduce the time of a brute-force attack on AES. True or false?
Ans: False; communication security, not encryption breaking, is the goal of quantum cryptography. Quantum computers can hack RSA using Shor's method.

Q4: Quantum cryptography is about techniques to break RSA. True or false?
Ans:   False.  Secure communication is the goal of quantum cryptography, not RSA cracking. Shor's algorithm can be used by quantum computing to crack RSA.

Q5: Quantum entanglement enables teleportation, which allows faster-than-light communication. True or false?
Ans: False; entanglement does not carry valuable information more quickly than light; it just shows the correlation between particles.

Q6: What is the name of the algorithm that can be used to break RSA?
Ans: Shor’s algorithm.

Q7: BB84 has a similar aim to which classical cryptographic algorithm?
Ans: Exchange of Diffie-Hellman keys. Keys can be safely shared using both.

Q8: BB84 has a similar aim to which classical cryptographic algorithm?
Ans: While most companies' prototypes have between 50 and 100 qubits, others have over 1000.

Task 2: Security Project
I worked on setting up and testing the various parts of our security project. I confirmed that all of the cloud virtual machines could be accessed via SSH by using netcat to check connections between them. I also set up an Apache web server and used tcpdump to capture HTTPS traffic and curl to access the server. I also added AES encryption and Diffie-Hellman key exchange to the client script to securely generate a shared key. These exercises helped me better grasp how secure communication is formed in real-world systems and how different cryptographic techniques work together to protect data.

Reflection:
This week, I learned the principles of quantum computing and its implications for cryptography. I examined how qubits can exist in superposition and how quantum algorithms like Shor's and Grover's might undermine traditional encryption methods like RSA and AES. I also understood the differences between quantum cryptography and quantum computing, especially how BB84 is different from conventional key exchange. While I temporarily continued working on the security project, I verified the encryption setup and tested connection. All in all, this week improved my understanding of future cryptography challenges and quantum-secure communication.
