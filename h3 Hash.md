## h3 Hash

_You'll use hashes for fingerprinting files, protecting passwords and as Bitcoin puzzles. You'll also take the role of the attacker, and crack some hashes with a well known tool, Hashcat._

# x) Read and summarize (with some bullet points)
Source: _Schneier B. 2015. Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition. Wiley._

2.3 2.3 One-way Fuctions" and "2.4 One-Way Hash Functions

- Easy to calculate but hard to reverse (practically impossible) - not possible to create a same pre-image that hashes the same way
- A trapdoor one-way function - possible to compute a function to other direction if a secret is known
- A one-way hash function (fingerprint, cryptographic checksum etc. many names)
  - An input string (pre-image) is converted to a fixed length output string (hash value)
  - A hash can be same for a pre-image - no certainty but reasonable accuracy to interpret that the strings are equal
  - A hash function can be computed other way pretty easily from a certain byte value and generate XOR values for it
  - A hash is public - The security lies in its one-wayness.
  - Single-bit change in the pre-image changes half a all the bits in the hash
  - A hash works like a certificate of authenticity - if someone hash a correct hash value you can be sure that he has the original file
  - A message authentication code (MAC) / Data authentication code (DAC) - 1 way hash function with a secret key - only the one who has the key can verify the hash value.
 
Karvinen 2022: Cracking Passwords with Hashcat_

Source _https://terokarvinen.com/2022/cracking-passwords-with-hashcat/_

- Hashcat is a password cracking tool 
- Hashcat tries every word in a dictionary to find if it matches the password

- Installed the needed apps: ![image](https://github.com/user-attachments/assets/4945dafb-94f2-4c15-8d66-58e3651524ba)
-  Created a directory for the work: ![image](https://github.com/user-attachments/assets/896b9d9a-c4dd-4958-a200-e77a73af274f)
- Got a dictionary (Rockyou): ![image](https://github.com/user-attachments/assets/a432a549-5ad4-4b9e-b004-85954460a040)
- Use tar -tool to extract file:![image](https://github.com/user-attachments/assets/525eed53-4a8e-45b8-b31d-ae0b4b15c7cf)

Identify Hash Type

- Type of the hash needs to be known to crack (number for the parameter -m)
- Hashcat does it for you with the command: $ 'hashid -m "insert hash here"'
![image](https://github.com/user-attachments/assets/77baa2d7-e17c-434b-8c7e-66212edc3c66)
- The right type is usually in the top three of the list
- Selected md5 because it's very common hash type

Crack The Hash
- Used the MD% (Hashcat mode: 0): ![image](https://github.com/user-attachments/assets/3624936a-f966-402b-8731-12a08ccceaca)
- Password is summer: ![image](https://github.com/user-attachments/assets/057069a7-15ed-4141-9032-1126e8814837)

What Did Hashcat Say?

- If Status in the Hashcat out is Exhausted it would mean that all words in the dictionary were tried but non of the worked:
![image](https://github.com/user-attachments/assets/c6a437e4-3f20-4657-a012-8215271ab106)
- Now the status was 'Cracked', Hashtype was MD5 and the target was the inputted hash 

Where Did the Solution Go?

- In the file 'solved' but it's also possible to see with a command $ 'hashcat -m 0 6b1628b016dff46e6fa35684be6acc96 rockyou.txt --show'
![image](https://github.com/user-attachments/assets/f910744e-f197-4626-9ff1-7beb8c1048be)

a) Billion dollar busywork. 
_Command 'echo -n "hello"|sha256sum' prints a hash. Try adding something to the string, e.g. 'echo -n 'hello asdf'|sha256sum'. What do you have to add to get a hash that starts with a zero? (Voluntary bonus: How is this related to Bitcoin? Voluntary difficult bonus: How many zeros can you get to the beginning? Voluntary difficult bonus: How does the difficulty raise?)_

Source: _https://terokarvinen.com/trust-to-blockchain/#homework_

![image](https://github.com/user-attachments/assets/ba76ee68-d918-4ce5-bece-9e13dcdb4816)
- Tried "Hello Molly".

![image](https://github.com/user-attachments/assets/8381e282-8566-4430-a77c-84835b4c63e8)

- The correct string was found right away. But why the first letter changed to zero?
https://bitcoin.stackexchange.com/questions/102414/how-does-solving-a-block-work-in-relation-to-the-first-letter-number-after-the-0

**b) Compare hash. Create a small text file. Take it's hash (e.g. 'sha256sum tero.txt'). Change one letter. Take the hash again. Compare hashes. What do you notice?**

- micro tomi.txt

![image](https://github.com/user-attachments/assets/47122444-b90d-46f3-bd49-31c30b7ccdbe)
- Changed one letter ('p' to 's') in the file: ![image](https://github.com/user-attachments/assets/c40f85eb-5a70-4cd6-b63d-d52cccd862e2)

![image](https://github.com/user-attachments/assets/3dbc0ec0-f316-4863-ba47-8443c6d22839)
- The change of just one character in the text file generated a completely different hash. 

**c) Hashcat. Install hashcat and test that it works.**

Installed and tested while summarizing the instructions on page https://terokarvinen.com/2022/cracking-passwords-with-hashcat/. Screens and workflow in the summary.

**d) Dictionary attack. Crack this hash: 21232f297a57a5a743894a0e4a801fc3**

Source: _https://terokarvinen.com/2022/cracking-passwords-with-hashcat/_

- Cracked the hash with Hashcat
  - $ 'hashcat -m 0 '21232f297a57a5a743894a0e4a801fc3' rockyou.txt -o solved'
- The hash was 'admin' (I used the same file as with the previous hash so there are two rows in the file)
- 
![image](https://github.com/user-attachments/assets/7219b533-1e20-4b3a-bda4-485ed4fe34c0)

**e) How can you make a password that's protected against a dictionary attack?**

My own pundering before using sources: Use a good password. e.g. a word that does not mean anything, Adding numbers and special characters to a password. 

From the source: _https://www.csoonline.com/article/569677/what-is-a-dictionary-attack-and-how-you-can-easily-stop-them.html_
- Use unique passwords which is a combination of random words, symbols and numbers.
- Don't reuse the password
- You can also use a passphrase (practically impossible to guess) like 'I want to be the best hacker in the world' - '! want TO b3 th3 B3st Hack3r !n th3 W0rld'.

**j) John. Install Jumbo John (John the Ripper, open source Jumbo version). Compile it from source code as needed. See Karvinen 2023 Crack File Password With John.**

Source: _https://terokarvinen.com/2023/crack-file-password-with-john/_

Cracking a ZIP archive password.
- $ sudo apt-get update
- In the instructions there was a following commnad for installing tools and libraries: 
  - $ 'sudo apt-get -y install micro bash-completion git build-essential libssl-dev zlib1g zlib1g-dev zlib-gst libbz2-1.0 libbz2-dev atool zip wget'

![image](https://github.com/user-attachments/assets/522b2c95-8f69-4349-8a5b-36ace2e64b50)

  - I had to remove 'zlib-gst' from the command because it was not found. Without it installation was ok. Let's see if it's possbile to do the task without it. 

Download & Compile John the Ripper, Jumbo version
- $ 'git clone --depth=1 https://github.com/openwall/john.git'
  
![image](https://github.com/user-attachments/assets/9de9eb2f-e790-4d30-8e41-77a3e5793d4b)

- $ 'cd john/src/'	
- $ './configure'
- $ 'make -s clean && make -sj4'
- Let's see if we get any warnings regarding 'zlib-gst' during compilation. -> No warnings regarding zlib-gst. There were other warnings but they don't seem to be important.

![image](https://github.com/user-attachments/assets/de2c436f-c033-4fb5-b5c2-b5a0ec8e686a)

- Many new executable in the run -folder:

- ![image](https://github.com/user-attachments/assets/5cd051fc-260e-49b1-a026-6a06f997e89c)

- Run John

![image](https://github.com/user-attachments/assets/25943b6d-6ef4-43d8-a3b1-e018b76b9dba)

**k) Crack file password with John.**

Source: _https://terokarvinen.com/2023/crack-file-password-with-john/_
Password Protected ZIP

- $ 'wget https://TeroKarvinen.com/2023/crack-file-password-with-john/tero.zip'
- Try to open:

  ![image](https://github.com/user-attachments/assets/e3fd404d-c1fd-4b7d-957a-9c3459507a98)

- Crack ZIP Password
- Extract the hash from the zip-file
- $ '$HOME/hashed/john/run/zip2john tero.zip >tero.zip.hash'

![image](https://github.com/user-attachments/assets/08d9344b-ad91-4328-b606-5407ed3d0181)

- Run a dictionary atack against the created hash:
- $ '$HOME/hashed/john/run/john tero.zip.hash'
  
![image](https://github.com/user-attachments/assets/5f1cd93a-4397-478c-9d54-82f66475b525)

- The password is 'butterfly'
- Unzip and open the content of the file:

![image](https://github.com/user-attachments/assets/8319315c-42de-465b-a59b-6618a3b68583)

