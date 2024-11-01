# h2 Pubkey (homework) 
Source: https://terokarvinen.com/trust-to-blockchain/#homework

## x) Summaries

€ Schneier 2015: Applied Cryptography: Chapter 2 - Protocol Building Blocks, sections

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

€ Rosenbaum 2019: Grokking Bitcoin:
Chapter 2. Cryptographic hash functions and digital signatures:
Digital signatures (8 sections, from "Typical use of digital signatures" to "Private key security")

Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg

## a) Pubkey today 
  Explain how you have used public key cryptography today or yesterday, outside of this homework. 
In addition to naming the system, identify how different parties use keys in different steps of the system. 
  (Answering this question likely requries finding sources on your own. This subtask does not require tests with a computer.)

asuntokauppa
Nettipankki
Source: 

  
## b) Messaging 
  Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. 
  Don't use Tero as a name of any party, unless that's your given name.)
  
## c) Other tool 
  Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen.
  
## d) Eve and Mallory
  In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. 
  Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)

## f) Password management
Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)

## g) Refer to sources 
Verify each homework report (this and the earlier ones) refers to sources. Every homework report should refer to this task page. It should also have references to any other source used, such as web pages, LLMs, man pages, other reports... References are mandatory, and must be present in every report. (This subtask does not need a report, you can just do it and write "Done." as the answer for this subtask.)
