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
