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

- In the file 'solved' but lso possbile to see with a command $ 'hashcat -m 0 6b1628b016dff46e6fa35684be6acc96 rockyou.txt --show'
![image](https://github.com/user-attachments/assets/f910744e-f197-4626-9ff1-7beb8c1048be)


a) Billion dollar busywork. Command 'echo -n "hello"|sha256sum' prints a hash. Try adding something to the string, e.g. 'echo -n 'hello asdf'|sha256sum'. What do you have to add to get a hash that starts with a zero? (Voluntary bonus: How is this related to Bitcoin? Voluntary difficult bonus: How many zeros can you get to the beginning? Voluntary difficult bonus: How does the difficulty raise?)


b) Compare hash. Create a small text file. Take it's hash (e.g. 'sha256sum tero.txt'). Change one letter. Take the hash again. Compare hashes. What do you notice?


c) Hashcat. Install hashcat and test that it works.


d) Dictionary attack. Crack this hash: 21232f297a57a5a743894a0e4a801fc3


e) How can you make a password that's protected against a dictionary attack?


j) John. Install Jumbo John (John the Ripper, open source Jumbo version). Compile it from source code as needed. See Karvinen 2023 Crack File Password With John.


k) Crack file password with John.
