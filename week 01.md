Week 1:
Q2: Install Ubuntu Linux
 <img width="259" height="200" alt="image" src="https://github.com/user-attachments/assets/b167e8f1-5f72-47fa-be65-782fc8efa403" />

Fig a: 
 I download the virtual oracle box and created week 1 linux as  seen in fig  a
And started using Ubuntu. As seen in fig b.
 
              [fig: b]
<img width="302" height="254" alt="image" src="https://github.com/user-attachments/assets/4a0e1391-c09e-4eef-9a59-8b1e01b6abb6" />



3.	Q3: Create your Git repository

I already have a GitHub account, and I created and configured the journal repository using GitHub Classroom. The README.md provides links to Moodle, study resources, and term progress in addition to a list of weekly tasks. The journal files for the first, second, and third weeks are organised well.
 <img width="452" height="282" alt="image" src="https://github.com/user-attachments/assets/ba5047ea-62d1-4a19-aac8-629a68116863" />

Q4: Setup your Git repository in Linux
<img width="452" height="210" alt="image" src="https://github.com/user-attachments/assets/9b050a44-25d6-4b80-9a44-d5592aae4018" />

<img width="314" height="344" alt="image" src="https://github.com/user-attachments/assets/7eb99168-3570-4e06-8d32-53c3b4290b19" />


 
 
I have created an SSH key for accessing  GitHub through the Vm as seen in above fig. 

Q: 5: Install pycipher for Python
<img width="278" height="112" alt="image" src="https://github.com/user-attachments/assets/8ac6f53e-1bfd-44d0-992a-d9a4ec19843c" />
<img width="336" height="79" alt="image" src="https://github.com/user-attachments/assets/4e82e106-641f-4353-af2a-dd852e93c00e" />

[installed pycipher for python]

Python 3, pip, and build-essential compilers were installed using the terminal. This guarantees Python scripting and necessitates properly operating cryptography software (such as pycipher) in the Linux environment.
Q 6: PyCipher Installation in a Virtual Environment.

<img width="252" height="172" alt="image" src="https://github.com/user-attachments/assets/e558b1ae-be71-499f-bde9-1fdf1379ec67" />

 
The pycipher module was successfully installed using pip, and the Python virtual environment was established and activated. Cryptography exercises can now start after installation was verified with a test command.
Q 7: Connect to Linux from Windows.
 
<img width="452" height="230" alt="image" src="https://github.com/user-attachments/assets/97d58224-3f5b-447e-83dc-da9befee41ea" />

[port forwarding in VM]


Configured port forwarding: I can securely connect via SSH to the Ubuntu virtual machine (VM) from localhost by mapping host port 2201 to guest port 22.
 <img width="345" height="330" alt="image" src="https://github.com/user-attachments/assets/d6115b8a-781b-44ce-91c1-05684d1e460d" />

[putty SSH Configuration]
To connect via SSH to an Ubuntu virtual machine, set up PuTTY on Windows and use the 127.0.0.1 IP address and host port 2201. This arrangement enables smooth remote terminal access throughout the term. so that I may connect to the virtual machine via putty with ease.

 <img width="186" height="148" alt="image" src="https://github.com/user-attachments/assets/fd79cc77-286d-4385-8327-d99f9f4821ad" />

[FileZilla file transfer setup]
The Ubuntu virtual machine was connected via SFTP using FileZilla (127.0.0.1:5022). successfully accessed and browsed Linux directories using Windows. I used 5022 as the port of my other PC to set up FileZilla, so this setup makes file sharing easy throughout the time. 
