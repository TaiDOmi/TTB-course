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

a) Billion dollar busywork. Command 'echo -n "hello"|sha256sum' prints a hash. Try adding something to the string, e.g. 'echo -n 'hello asdf'|sha256sum'. What do you have to add to get a hash that starts with a zero? (Voluntary bonus: How is this related to Bitcoin? Voluntary difficult bonus: How many zeros can you get to the beginning? Voluntary difficult bonus: How does the difficulty raise?)


b) Compare hash. Create a small text file. Take it's hash (e.g. 'sha256sum tero.txt'). Change one letter. Take the hash again. Compare hashes. What do you notice?


c) Hashcat. Install hashcat and test that it works.


d) Dictionary attack. Crack this hash: 21232f297a57a5a743894a0e4a801fc3


e) How can you make a password that's protected against a dictionary attack?


j) John. Install Jumbo John (John the Ripper, open source Jumbo version). Compile it from source code as needed. See Karvinen 2023 Crack File Password With John.


k) Crack file password with John.
