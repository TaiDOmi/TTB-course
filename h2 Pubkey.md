# h2 Pubkey (homework) 
Source: https://terokarvinen.com/trust-to-blockchain/#homework

## x) Summaries

**Schneier 2015: Applied Cryptography: Chapter 2 - Protocol Building Blocks, sections**

Source: Schneier B. 2015. Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition. Wiley. 

2.5 Communications Using Public-Key Cryptography
- Cryptography based on key pairs: a public and a private key ("a cryptographic safe")
- Public key is used to encrypt a message & Private key is used to decrypt a message
  - Example: Sending email to one's mailbox (public key) - Opening the email and reading it (private key)
  - Decryption is extremely hard without the private key
- Hybrid cryptosystem: public-key cryptography is used to distribute session keys.
  - A session key is generated when it is needed and destroyed after it is no loger needed (eg. temporary session keys)
  
2.6 Digital Signatures
- A digital signature 
  - is authentic 
  - cannot be falsified (signer is the correct person because all parties know that only he knows the private key)
  - Cannot be reused in another document
  - The document cannot be altered after signed
  - The authenticity of the signature cannot be denied afterwards
- A digital signature trees
  - A scheme of infinite amount of one-time signatures
  - root in a public file authenticates sub-nodes and so on
- Signing documents with public-key cryptography
  - either public or private key can be used for encryption
  - encrypt the document with private key by signing it and send to receiver who decrypts the doc with sender's public key
-  Time-stampts are used to verifyif signature has been already used (eg. bank checks from a check's timestamp if it has been already used).
-  Digital signatures with one-way hash functions to save time (only hash is signed)
  - Benefits: signatue separate from the doc, storage reqs for storing are smaller
- Algorithms and terminology
  - Several digital signature algorithms (all with private and public key)
  - Many can be used for signatures but not for encryption
- Multiple signatures
  - Two ways: Both have their separate copies of the doc signed or the second signs the first signature (need both keys to verify)
- Possible to cheat if the signer 'loses' the key and claims that she did not sign the document (repudiation).
  - Timestamps can help with this eg. old signatures cannot be invalidated by invalidating eg. a bank account
  
2.7 Digital Signatures With Encryption
- A digital signature combined with public-key encryption
  - Signing before encrypting 
  - Two key pairs (encryption and signature)
  - Confirmation of messages received to sender that recipient has received the message
- Attacks
  - Public keys can be stolen from public databases
  - An authority eg. Key Distribution Center (KDC) can be used to prevent substituting public keys
    - KDC signature assures the validity of the public key
    
2.8 Random And Pseudo-Random-Sequence Generation
- Computers are predictable (periodical numbers that repeat) when generating random numbers
- Cryptography uses sensitive properties to ensure that the number is random
- Cryptographically secure pseudo-random-sequences
  - unpredictable, infeasible to predict next random bits (even if full knowledge of the algorithm and previous bits in the stream)
  - Still possible to break
  - Cryptography = Making generators resistant to attack 
- Real randomness
  - Cannot be reliable reproduced (even with similar inputs), two copmletely random sequences as a result
- Three properties for generator
  - looks random, unpredictable, cannot be reliable reproduced 

**Digital signatures**

Source: Rosenbaum K. 2019. Grokking Bitcoin. Manning Publications.

Typical use of digital signatures
- Step 1: preparation (make a private key and then public key which is calculated from the private key + give the public key to receiver)
- Step 2: signing (Write email with an attachment which is signed with the private key) and sent email
- Step 3: Verifying (The receivers verifies the signature and the attachment with the public key)
- A key pair can be reused
- A random number generator is used to generate 256-bit random number (available on operating systems)
- The private key cannot be generated from the public key
- The public key is alwasys the same when it's generated from the same private key
- The public key is longer (33 bytes) than the private key (32 bytes)

Two ways to use the key pair
- Encrypt with public key and decrypt with the private key
- Encrypt with private key and decrypt with the public key

Private Key security 
- Private key needs to be protected at all costs (up to the owner)
- Cannot be restored if lost
- Need to be stored in an encrypted file with a strong password
- Great security: Offline, encrypted file and split the key (eg. three parts on different devices)

**Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg**

Source: https://terokarvinen.com/2023/pgp-encrypt-sign-verify/

PGP encryption with 'gpg' tool
- Linux Kernel development uses PGP signatures
- Install tools
- Generate keypair
- Print keypair
- Export public key
- Check public Key 
- Create folder to simulate the recipient
- Create a keypair to recipient
- Import and verify sender's key
- Sender needs to know that recipient is the correct person (recipient's public key is needed)
  - Both parties need to know they ha correct public keys
-  When trust is established a secret message can be sent
 

## a) Pubkey today 
_Explain how you have used public key cryptography today or yesterday, outside of this homework. 
In addition to naming the system, identify how different parties use keys in different steps of the system. 
  (Answering this question likely requries finding sources on your own. This subtask does not require tests with a computer.)_

Digital signature of the apartment's deed of sale 
- DIAS service (digitaalinen suntokauppa)
  - three parties need to sign (two sellers and one buyer) + apartment dealer
  - Apartment deed is created in digital form to (DIAS system) by the apartment dealer (creates hash fingerprint for the deed. 
  - DIAS system sends invitations to all three parties by email to sign the document
    - Step 1: DIAS system prepares separate private keys (from hash) for both sellers and the buyer and then public key (which is calculated from the private keys)
  - Parties use public key cryptography to sign the document
    - Step 2: signing (System sends email with an attachment which is signed with the private key) 
    - Step 3: Verifying (The receivers verifies the signature and the attachment with the public key) by creating a new hash from the deed and compares hashes of the signed and the new hash. If they match signing is valid.
      
Sources: 

Rosenbaum K. 2019. Grokking Bitcoin. Manning Publications.

https://www.theseus.fi/bitstream/handle/10024/496522/kuhlberg_joel.pdf;jsessionid=5C656AD3DB64691E6F8AF746BBF92EFD?sequence=2

https://www.theseus.fi/bitstream/handle/10024/347237/Tormala_Nina.pdf?sequence=2

## b) Messaging 
_Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. 
Don't use Tero as a name of any party, unless that's your given name.)_

- Install tools
  - "$ sudo apt-get update" / Update the package manager.
  - "$ sudo apt-get install gpg micro psmisc" / Install 'gpg' encryption tool.
- Generate keypair
  - gpg --gen-key
    - ![image](https://github.com/user-attachments/assets/b9b9bc00-fa6d-4fbf-a2a0-ead6df4a1e0f)
- Print keypair
  - ![image](https://github.com/user-attachments/assets/6d01821b-184f-4d20-b0f6-268c5cd451df)
- Export public key
- Check public Key 
- Create folder to simulate the recipient
- Create a keypair to recipient
- Import and verify sender's key
- Sender needs to know that recipient is the correct person (recipient's public key is needed)
  - Both parties need to know they ha correct public keys
-  When trust is established a secret message can be sent
  
## c) Other tool 
_Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen._

Source: https://www.mv.helsinki.fi/home/jussantt/linux/keyident.html

OpenSSH
1. Create a key pair with default settings "$ ssh-keygen -t rsa"
2. 
  
## d) Eve and Mallory
_In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)_

## f) Password management
_Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)_

## g) Refer to sources 
Done
