# h2 Pubkey (homework) 
Source: _https://terokarvinen.com/trust-to-blockchain/#homework_

## x) Summaries

**Schneier 2015: Applied Cryptography: Chapter 2 - Protocol Building Blocks, sections**

Source: _Schneier B. 2015. Applied Cryptography: Protocols, Algorithms and Source Code in C, 20th Anniversary Edition. Wiley._

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

Source: _Rosenbaum K. 2019. Grokking Bitcoin. Manning Publications._

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

Source: _https://terokarvinen.com/2023/pgp-encrypt-sign-verify/_

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
- Import and verify recipient's key
  - Both parties need to know they have correct public keys
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

_Rosenbaum K. 2019. Grokking Bitcoin. Manning Publications.

https://www.theseus.fi/bitstream/handle/10024/496522/kuhlberg_joel.pdf;jsessionid=5C656AD3DB64691E6F8AF746BBF92EFD?sequence=2

https://www.theseus.fi/bitstream/handle/10024/347237/Tormala_Nina.pdf?sequence=2_

## b) Messaging 
_Send an encrypted and signed message using PGP, then verify and decrypt it. (You can use folders to simulate users, or use two computers or two different OS users. 
Don't use Tero as a name of any party, unless that's your given name.)_

- Install tools
  - $ 'sudo apt-get update' / Update the package manager.
  - $ 'sudo apt-get install gpg micro psmisc' / Install 'gpg' encryption tool.
- Generate keypair
  - $ 'gpg --gen-key'
  - ![image](https://github.com/user-attachments/assets/b9b9bc00-fa6d-4fbf-a2a0-ead6df4a1e0f)
- Print keypair
  - ![image](https://github.com/user-attachments/assets/6d01821b-184f-4d20-b0f6-268c5cd451df)
- Export public key
  - $ 'cd' / Go to home directory. 
  - $ 'gpg --export --armor --output tomi.pub' / (export public key, with ASCII characters and output it into the file tomi.pub)
- Check public Key
  - $ 'head -4 tomi.pub'
  - ![image](https://github.com/user-attachments/assets/14686506-18c3-4964-b477-423b472214e1)
- Create folder to simulate the recipient
   - $ 'cd' / Go to home directory.
   - $ 'mkdir liisa/' / Make a folder to Liisa to simulate another user. 
   - $ 'chmod og-rwx liisa/' / Protect the folderby removing read, write, and execute permissions for all users except the file's owner.
- Simulate the recipient (Liisa) and work from her folder
  - $ 'cd liisa/'
  - $ 'gpg --homedir . --fingerprint' / replace 'gpg' with 'gpg --homedir (in every command)
 ![image](https://github.com/user-attachments/assets/f8aed324-cb77-4087-8ada-e847a250eb7c)

- Create a keypair to recipient (Liisa)
  - $ 'gpg --homedir . --gen-key'
  - $ 'gpg --homedir . --fingerprint'
  - ![image](https://github.com/user-attachments/assets/db91fa22-7081-4fe4-8f35-97ec32507950)
- Import and verify sender's key
  - $ 'cd' / go to home directory where the public key (tomi.pub) is saved.
  - $ 'cp -v tomi.pub liisa/' / Copy the exported public key as Liisa is simulated
  - ![image](https://github.com/user-attachments/assets/44446a8e-8ed2-446c-aa77-5849dde7bb57)
  - ![image](https://github.com/user-attachments/assets/bc8e6531-4778-41a5-80a0-8dc5dd7fa856)
  - $ 'gpg --homedir . --fingerprint' / Import and verify Tomi's Key - public keys match
  - ![image](https://github.com/user-attachments/assets/d549bde9-e47a-42ee-8f21-0cfd77e8fd1c)
  - $ '$ gpg --homedir . --sign-key "_insert key here_"' / Liisa signs Tomi's key to mark it as trusted
  - ![image](https://github.com/user-attachments/assets/11cce1c1-2735-4443-a15b-60c92bb996eb)
- Import and verify recipient's key
  - $ gpg --homedir . --export --armor --output liisa.pub
  - $ cp -v liisa/liisa.pub .
  'liisa/liisa.pub' -> './liisa.pub'
  - ![image](https://github.com/user-attachments/assets/437eca39-7f59-488e-8056-2c205ac0b7a6)
  - $ 'gpg --import liisa.pub' / Tomi imports Liisa's key
  - $ '$ gpg --sign-key "_insert key here_"' / Tomi signs Liisa's key to mark it as trusted
  - ![image](https://github.com/user-attachments/assets/9d0f8707-43bc-4cdd-bd74-bb1541577739)
  
Trust established
-  When trust is established a secret message can be sent
- / Liisa sends message to Tomi
  - $ cd ~/liisa/
  - $ micro miniviesti.txt
  - ![image](https://github.com/user-attachments/assets/93080086-fd33-4215-832d-63f1d20f8f2c)
  - $ 'gpg --homedir . --encrypt --recipient taidomi@gmail.com --sign --output encrypted.pgp --armor miniviesti.txt'/ Encrypt and sign the message.
  - ![image](https://github.com/user-attachments/assets/db314e46-69a3-42d1-a27f-73373527e0ea)
  - Encrypted message was generated.
  - ![image](https://github.com/user-attachments/assets/c999591a-3ce9-4384-a569-ba7dba922ead)
  - $ 'cp -v liisa/encrypted.pgp .'/ Copy the file to Tomi
'liisa/encrypted.pgp' -> './encrypted.pgp'
  - $ 'gpg --decrypt encrypted.pgp' / Decrypt the file.
![image](https://github.com/user-attachments/assets/094d0fdc-c239-4d21-a975-d8e5c3ba1db4)

## c) Other tool 
_Encrypt a message using a tool other than PGP. Explain how different parties use different keys at different stages of operation. Evaluate the security of the tool you've chosen._

Sources: _https://medium.com/akatsuki-taiwan-technology/encrypt-using-ssh-key-pair-f7e99dfef164
https://www.digitalocean.com/community/tutorials/understanding-the-ssh-encryption-and-connection-process_

Encrypted messaging with Secure Shell (SSH)

OpenSSH
- Install tools
  - $ 'sudo apt-get update' / Update the package manager.
  - $ 'sudo apt-get install openssh-server' / Install open-ssh encryption tool.
- Generate keypair (to Sender 'Tomi)'
- Create a key pair with default settings "$ ssh-keygen -t rsa"
  - ![image](https://github.com/user-attachments/assets/293982fe-17d0-4b57-aa6e-338e26092552)
  - Keys (private 'id_rsa' & public 'id-rsa.pub') were generated into subdirectory .ssh
![image](https://github.com/user-attachments/assets/9675fa2f-eccc-428c-afc0-add6b121b2b4)
  - Need to convert the public key into PKCS8 format (to use with openssl)
  - ![image](https://github.com/user-attachments/assets/60985dbc-259e-4347-92d9-3f42a6392142)
  - ![image](https://github.com/user-attachments/assets/b6785be5-f557-4560-8892-75053e0de4e4)

- Generate keypair (to Receiver 'Liisa')'
- Create a key pair with default settings "$ ssh-keygen -t rsa"
  - Made a directory to key 'mkdir .ssh' under Liisa's folder because for some reason keygen could not do the sub-folder automatically for Liisa.
  -  ![image](https://github.com/user-attachments/assets/0035828a-de9a-426c-b8f6-bfb70b4bc9c9)
  -  ![image](https://github.com/user-attachments/assets/da428288-c614-4758-9d2d-affefa385bd5)
-  Import and verify sender's key
  - $ 'cd/home/tomik/.ssh' / go to home directory where the public key (is_rsa.pub.pkcs8) is saved.
  - $ 'cp -v id_rsa_pub.pkcs8 /home/tomik/liisa/.ssh' / Copy the exported public key to Liisa's .ssh folder
  - Convert Liisa's public key to PKCS8 format:
    - $ 'ssh-keygen -e -f ./id_rsa_liisa.pub > id_rsa_liisa_pub.pkcs8'
    - ![image](https://github.com/user-attachments/assets/d87eb140-8555-4dd7-adb6-b43be278ae5b)
  - Liisa has now both public keys
  - ![image](https://github.com/user-attachments/assets/335debea-5034-4e31-8500-b77dafe1234a)
- Liisa creates a message to Tomi
  - $ 'micro miniviesti2.txt'
  - ![image](https://github.com/user-attachments/assets/5e01c2a1-4912-4344-a1a3-0cd0816b5c6a)
  - Encrypt a message using Tomi's public key:
    - $ 'cat miniviesti2.txt | openssl rsautl -encrypt -pubin -inkey id_rsa_pub.pkcs8 > miniviesti2.enc' -> For som reason I cannot encrypt the message because system cannot read public key
   ![image](https://github.com/user-attachments/assets/e22d80a1-4990-409b-be80-9c55152ed90a)
    - The public key:  
    - ![image](https://github.com/user-attachments/assets/7b9675a8-7440-4283-89e7-9893c8b08dfb)

  - $ 'cp -v liisa/.ssh/miniviesti2.enc /home/tomik/.ssh'/ Copy the file to Tomi
'liisa/encrypted.pgp' -> './encrypted.pgp'
  - $ 'gpg --decrypt encrypted.pgp' / Decrypt the file.

**Tried to do the same with genpkey, pkey and pkeyutil -tools**

Source: _https://medium.com/sureshatt/public-key-cryptography-with-openssl-bdaf39410a53_
- Created a keypair for Tomi with genpkey -tool (The generated file contains both keys.)
  - $ 'openssl genpkey -algorithm RSA -pkeyopt rsa_keygen_bits:1028 -outform pem -out rsakey.pem -aes192'
- Extracted the public key with pkey-tool
  - $ 'openssl pkey -in rsakey.pem -out rsapubkey.pem -outform pem -pubout'
- Copied the public key to liisa
  - $ 'cp -v rsapubkey.pem /home/tomik/liisa/'
- Generate Keypair to Liisa
  - $ 'openssl genpkey -algorithm RSA -pkeyopt rsa_keygen_bits:1028 -outform pem -out liisarsakey.pem -aes192'
- Extracted the public key with pkey-tool for Liisa
  - $ 'openssl pkey -in liisarsakey.pem -out liisarsapubkey.pem -outform pem -pubout'
- Liisa create's a text file and signs it with pkeyutl-tool
  - $ 'micro liisaviesti.txt'
  - $ 'openssl pkeyutl -sign -in liisaviesti.txt -inkey liisarsakey.pem -out sigliisaviesti.txt'
- Verify signature with public key
  - $ 'openssl pkeyutl -verify -pubin -inkey liisarsapubkey.pem -sigfile sigliisaviesti.txt -in liisaviesti.txt'
  - ![image](https://github.com/user-attachments/assets/689e18b3-06f0-4eb2-9623-3143d67b74b5)
- Liisa encrypts the message with Tero's public key
  - $'openssl pkeyutl -encrypt -pubin -inkey rsapubkey.pem -in data.txt -out encliisaviesti.txt'
- Send the encrypted message to Tomi
  - $ 'cd encliisaviesti.txt /home/tomik/'
- Tomi decrypts the message with private key
  - $ 'openssl pkeyutl -decrypt -inkey rsakey.pem -in encliisaviesti.txt -out decliisaviesti.txt'
  - ![image](https://github.com/user-attachments/assets/2b3f9a70-b4f1-4399-b4f7-1448f2a02246)

I did not find instructions to create trust with OpenSSL tool. Otherwise the encrypting process was pretty much the same that with PGP. It feels also that PGP is simpler to use than OpenSSL. 
Also I found that they seem to have a different purpose of use and suited for different security needs. PGP is more suitable for encrypting and signing messages and OpenSSH is focused on securing remote access. Both encrytption tools (PGP and OpenSSL) share the same risk of stolen or leaked private keys. _Source: ChatGPT: 'Compare security between PGP and OpenSSH security tools'_
  
## d) Eve and Mallory
_In many crypto stories, Eve is a passive eavesdropper, listening on the wire. Mallory malliciously modifies the messages. Explain how PGP protects against Mallory and Eve. Be specific what features, which use of keys and which flags in the command are related to this protection. (This subtasks does not require tests with a computer)_

Sources: _https://www.kernelconcepts.de/email-encryption-with-pgp/?lang=en
https://crysp.uwaterloo.ca/courses/cs458/F08-lectures/Module5.pdf
https://terokarvinen.com/2023/pgp-encrypt-sign-verify/_

PGP povides guard for both Eve (passive eavesdropper) and active attacker (Mallory).
Eve:
- Encryption with public key 
  - The sender encrypts the message with recipient's public key -> Eve cannot interpret the message even though she would have access to it
  -   - $ 'gpg --homedir . **--encrypt** --recipient tero@example.com.invalid --sign --output encrypted.pgp --armor message.txt'

Mallory:
- Digital signature verified with the sender's public key verifies that the message came from the sender unaltered. -> Prevents man in the middle attacks
  - $ 'gpg --homedir . **--encrypt** --recipient tero@example.com.invalid --sign --output encrypted.pgp --armor message.txt'
- Public key authentication verifications and signing the public keys prevent attacker from changing the public key. -> Mallory cannot impersonate the sender
  - Sender and receiver imports and validates each others public key:
  - $ 'gpg **--sign-key** "B20F D80B 705C 791D C878  0030 7BAA 4F13 2645 134F'
  - Endrypting and signing the message: $ 'gpg --homedir . **--encrypt** --recipient tero@example.com.invalid **--sign** --output encrypted.pgp --armor message.txt'
  - $ 'gpg --decrypt encrypted.pgp'
    - Signarure validation at the end of decrypted message
    - gpg: Signature made Fri 17 Nov 2023 12:52:22 PM EET
      gpg: using RSA key B20FD80B705C791DC87800307BAA4F132645134F
      gpg: Good signature from "Alice <alice@example.com.invalid>" [full]

## f) Password management
_Demonstrate use of a password manager. What kind of attacks take advantage of people not using password managers? (You can use any password manager, some examples include pass and KeePassXC.)_

Sources: _https://www.passwordstore.org/
https://www.theguardian.com/technology/2022/mar/19/not-using-password-manager-why-you-should-online-security_

Why to use password management system?
- No need to remember passwords
- Generate strong passwords and save them to the system
- Ensure unique login for each account -> Prevents credential-stuffing (Attacker uses password trying to get in other services eg. Tries if Facebook password applies to Netflix etc.)
- Prevent phishing attacks (Click a fake link to steal a password). Since credentials are saved for specific address they are filled automatically to fields. 


'Pass' password management system
- Passwords are saved in gpg encrypted file
- used with command line
- Sample commands:
  - $ 'pass' / List all passwords
  - $ 'pass Email/gmail.com' / Show password for gmail.
  - $ '$ pass -c Email/gmail.com / Copy to clipboard.
  - $ 'pass insert Business/Kauppalehti.fi' / Adding passwords to store
  - $ 'pass generate Email/JonDoe.com' / Generate random password
  - $ '$ pass rm Business/Kauppalehti.fi' / Remove password


## g) Refer to sources 
Done
