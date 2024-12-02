# h6 Upside Down Iceberg

## x) Read and summarize (briefly, e.g. with some bullets)
**Tor: The Second-Generation Onion Router**
Source: _Dingledine, Mathewson and Syverson 2004: Tor: The second-generation onion router. In USENIX security symposium (jufo level 2)_

3 Design goals and assumptions
Goals:

- The main goal of Tor is to make attackers efforts useless by prevent attackers from connecting users to their communicational partners.
- Easy and cheap to use - Must not require too much bandwith so that volunteers are found to run the network.
- Must not make operators liable to illegal user actions
- Good usability is not only for a convenience -> More users and better anonymity
  - Easy to implement on all common platforms
- Flexible and well defined protocol to be suitable as a platform for future development (no need to reinvent a wheel again)
- Design protocol and security parameters need to be well understood to provide secure and stable system.

Deferred goals (solved aleready elsewhere or no known solution yet):

- No peer-to-peer (high risk for attackers)
- No full protection aainst E2E attacks
- Tor does not automatically adjust protocols (E.g. HTTP) to hide users but users can use provoxy-tool to remove identity revealing information.
- Tor does not try to hide that someone is using the network


**Tor: The Second-Generation Onion Router**
Source: _Karunanayake, Ahmed, Malaney, Islam and Jha 2021: De-anonymisation attacks on tor: A survey. In IEEE Communications Surveys & Tutorials (jufo level 2)_

- Abstract
- I Introduction
- II Background (to the end of "B. Circuit Establishent for Tor HS")
- Fig. 6. Taxonomy for Tor attacks (Just the figure on page 2330.)

**PhishSticks - The Ethical Hackers tool for BadUSB**
Source: _https://www.youtube.com/watch?v=bDzVevtZiWE_

- A simulated attack by penetration tester
- He left a PhishStick (USB stick) to CEOs table
  - Demonstrate different payload
  - USB Dropper attack
  - Keylogger payload in this USB stick
  - When plugged in to Windows a Phishstick it uses injected kestrokes to open Run in Wondows and then fetches the payload from the internet in PowerShell
    - Difficult to notice as attack is shown only a short time on the screen
  - Then records all keystrokes by user (credentials)
  - keystrokes are stored in TEMP file and then send to hacker
  - logs are removed after they have been sent by HTTP POST
  - Consequences: Severe losses or leagal issues for the company
 
## a) Install TOR browser and access TOR network (.onion addresses). (Explain in detail how you installed it, and how you got access to TOR).

- $ 'sudo apt-get update' / update packages
- Tried to install via Terminal
  - $ 'sudo apt-get -y install tor torbrowser-launcher'
  - ![image](https://github.com/user-attachments/assets/3fc85f18-7473-4b9e-9504-b346a42eab8f)
  - Seems that the package is not currently available. 
- Download package from (https://www.torproject.org/download/)
- Clicked 'Download for Linux'.
- The package was downloaded to /home/tomik/Downloads
- ![image](https://github.com/user-attachments/assets/113790b9-bed8-4af3-8b83-83927fed5cc7)
- Extracted the package to /tmp
- Launched the TOR browser
- ![image](https://github.com/user-attachments/assets/5127161e-2c7f-4599-8ef9-0fcb991468d7)
- ![image](https://github.com/user-attachments/assets/8b7fccc6-8ca5-48af-a0db-758dece0cb3a)

## b) Browse TOR network.
- Find, take screenshots and comment
  - search engine for onion sites
  - human rights or civil rights organization
  - marketplace
  - fraud
  - forum
  - a well known organization (with regular postal addresses, offices or similar presence outside darknet)
- Use .onion addresses inside TOR network, not regular (clearnet) websites trough exit nodes.

## c) Onion. In your own words, how does anonymity work in TOR? (e.g. how does it use: public keys, encryption, what algorithms? This subtask does not require tests with a computer.)

## d) What kind of the threat models could TOR fit? (This subtask does not require tests with a computer.)

## e) Don't stick that stick. How does PhishSticks attack work? Would a typical organization be vulnerable? Does this link to a broader category of attacks and defenses? How could the risk be mitigated? (This subtask does not require tests with a computer.) (If you want, you can view PhishSticks on Github and PhishSticks Youtube channel.






