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
  - Anonymity networks are increasing their popularity
  - Tor is the most used browser to use anonymity networks
  - Anonymity can be misused (illegal site of selling illegal goods and services or sharing censored content)
  - As a result goverments and law enforcements are interested to find ways to de-anonymise users
- I Introduction
  - Privacy protection is needed for E.g.
    - people in totalitary countries .
    - military to keep operations safe
    - businesses to keep development and research safe
  - Onion Router project = Tor
    - Solved the low latency and availability problems of earlier anonymity networks.
    - Tool also for all kinds of criminal activity
  - The investigation concentrates on de-anonymization attacks from past surveys
    - 30 de-anonymization attacks discussed
    - Advances in security have made many previous attacks useless.
- II Background (to the end of "B. Circuit Establishent for Tor HS")
  - Tor is an overlay network based on TCP (three voluntary relays)
    - Onion proxy (Tor client): Installed to user's computer (establishes a connection to Tor network and handles connections)
    - Directory Servers: Small amount of trusted servers to keep details about the status of Tor network and select three relays.
    - Entry Node: The first node and the one that client connects directly
      - Many attacks to de-anonymise the user
    - Exit Node: Knows the IP of the destination server
    - Hidden / Onion Services: Hides the accessed website.
    - Introduction Points: Random nodes selected by onion services  (several selected to defend from DoS attacks) to register its services with Tor network.
    - Rendezvous Points: Random node that client connects at start
    - Bridges: Tor relays that are not listed publicly (to avoid shutting down services)
  - A. Standard Tor Circuit Establishment
    1. The installed onion proxy (OP) connects directory servers to get an active list of servers
    2. OP selects 3 relays  (entry, middle and exit nodes)
    3. OP  creates an circuit to alter encryption keys with nodes
    - Fixed length cells of 512 bytes are used for communication.
    - Relay header and payload are encrypted with 128-bit counter mode - Advanced Encryption Standard (AES)
  - B. Circuit Establishment for Tor Onion Services
    -  
- Fig. 6. Taxonomy for Tor attacks (Just the figure on page 2330.)
  - Main attack categories of Tor network
    - Network disruption attacks
    - De-anonymization attacks
    - Censorship Attacks
    - Generic Attacks

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
  - The default search engine DuckDuckGo does not search onion sites
    - Search onion search engine for onion sites
    - ![image](https://github.com/user-attachments/assets/d45bd52c-d111-41f5-983b-700efdd9aaeb)
    - Selected Ahmia as it was the first option:
    - ![image](https://github.com/user-attachments/assets/7dd961a0-49a9-4dc3-97b5-50f63f57ee13)
  - human rights or civil rights organization
    - Searched for 'human rights organization'
    - ![image](https://github.com/user-attachments/assets/8b8ee516-47fe-4fa3-a827-e623eded2dc9)
    - Found information how to keep corporate data safe from covernment monitoring
      - Like Keep your device well hidden, Install a privacy focused OS like Tails or Qubes
  - marketplace
    - Searched for Onion marketplace in Ahmia:
      -  Took the first link (venus marketplace)
      -  ![image](https://github.com/user-attachments/assets/070dcdb2-44e3-4641-8b80-d6ca00d79b4e)
  - fraud
    - Darknet marketplaces are full of frauds
    -  I searched in Ahmia: "How to order a fake bank statement"
    -  Took the first option
    -  ![image](https://github.com/user-attachments/assets/353eef20-740b-49bb-b221-0bb5878c378f)
  - forum
    - Searched "Darknet forum" in Ahmia and took the third search result "Forums".
    - ![image](https://github.com/user-attachments/assets/ab7c9524-37e1-4e18-b6c7-c95292f298d6)
    - ![image](https://github.com/user-attachments/assets/bab0ccc5-9ce8-4ad8-8b52-bfbb9fec49bd)
  - a well known organization (with regular postal addresses, offices or similar presence outside darknet)
      - Searched "Amnesty international" and took the first link as these sites might be the ones in dictature states monitored and onoin sites are needed to provide information also in those countries.
      - There was a link to Amnesty's website
      -![image](https://github.com/user-attachments/assets/ee29481c-df09-4a4f-8399-1467d9129348)
      - ![image](https://github.com/user-attachments/assets/bda70418-d9f6-4447-a3a6-8cd51af60424)
## c) Onion. In your own words, how does anonymity work in TOR? (e.g. how does it use: public keys, encryption, what algorithms? This subtask does not require tests with a computer.)
Sources: _https://tb-manual.torproject.org/about/, https://support.torproject.org/about/key-management/_

- Tor network protects your identity with a network of virtual tunnels using three random servers to send your traffic. Thus there is three servers between you and the traffic to public network.
- Tor uses TLS (Transport LaAyer Security) link encryption
- The client establishes a short lived encryption key for every Tor relay
- The public key is renewed every four weeks
  - Each node in Tor network has a key pair. The public key (onion key) of each nodeis used to encrypt the data. -> Your data is encrypted multiple times before it's sent to the network. 
- TOR uses strong algorythms like AES (Advanced Encryption Standard)
- Onion process (Each node in chain peels off a layer of the onion):
    1. Data is encrypted for the last (exit) node.
    2. After that the data is encrypted to the middle node.
    3. Data is encrypted to the first node
  - None of the dingle nodes knows the whole route.

## d) What kind of the threat models could TOR fit? (This subtask does not require tests with a computer.)

Sources: _[https://ieeexplore.ieee.org/abstract/document/9089497](https://www.researchgate.net/figure/The-Tor-website-fingerprinting-threat-model_fig1_329743510), https://security.stackexchange.com/questions/203361/can-javascript-break-anonimity-provided-by-tor, https://thehackernews.com/2018/09/tor-browser-zero-day-exploit.html, https://thehackernews.com/2017/11/tor-browser-real-ip.html_

- Website fingerprinting attacks can reveal pages users are visiting
  - Attackers  can guess the websites by analysing the patterns in data packets that have been sent and received.
  - They can use smart tools like neural networks (AI) to spot the patterns.
- Javascript could be used to run code on users computer or to reveal the location
  - Javascipt can also be deactivated in setting but then many websites stop working
- Not updating Tor browser could be dangerous (Zero-day exploits)
  - E.g. Bypassing NoSCript selection, Reveal users real IP address by running JavaScript on users TOR browser

## e) Don't stick that stick. How does PhishSticks attack work? Would a typical organization be vulnerable? Does this link to a broader category of attacks and defenses? How could the risk be mitigated? (This subtask does not require tests with a computer.) (If you want, you can view PhishSticks on Github and PhishSticks Youtube channel.

Sources: _https://www.youtube.com/watch?v=bDzVevtZiWE, https://github.com/therealhalonen/PhishSticks, https://www.teramind.co/blog/usb-blocking/, https://attack.mitre.org/matrices/enterprise/_

- A hacker could leave an USB stick to a workers table which then plugs it in the machine
  - AutoRun runs a malicious code which
    - E.g. records all the keystrokes and sends them to the hacker
    - Move other sensitive information ot the attacker
  - Also USB-device can be infected with malware that can cause different kind of problems E.g. Operational disruptions. 
- Any company with employees with poor information security awareness and without good information security policy is vulnerable to attacks.
  - People can also intentionally disregard secure ways of working.
- Phishstick attacks could be under Initial Access category and Phishing and content injection techniques (Mitre Enterprise Matrix).
- To protect from the attacks and mitigate the risk
  - Implement policies for USB blocking
    - Choose the right methods for the company needs.
    - Limit the USB port access
      - E.g. Block all USB devices or block USB ports from untrusted devices.
      - Admit only secure USB devices 
  - Train employees to be aware of secure ways of working.










