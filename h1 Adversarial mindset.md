# h1 Adversarial Mindset (homework)

## x) Summaries
**Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains**
Source:  (Hutchins et al 2011, https://www.lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)
- New class threats "Advanced Persistent Threat" (APT): Attackers are better resourced, organized and more skilled than before.
  - Long term hacking campaigns with advanced tools and methods that can break through the typical computer network security means.
  - Attackers learn and adapt intrusions based on what works or fails with each attempt. 
- Conventional security methods fail because of assumptions that action should be taken only after security breach has happened and that the problem that caused the breach is a fixable flaw.
  
- 'Kill chain' is a defence model to protect from attackers by understanding and breaking an attack down to phases.
  - The idea is to recognize patterns in attacks and improve defenses against attacks and improve the effectiveness of security investments.
  - Cut one chain (phase) to mitigate the attack
  - The method is called "Intelligence-driven computer network defense (CND)"

- Indicator: information that describes an intrusion
  - Atomic indicators: Cannot be broken doqn further (eg. IP, email, identifiers)
  - Computed indicators: Derived data related to an incident (regular expressions, hash data)
  - Behavioral indicators: Combinations of atomic and computed indicators (often with specific patterns). 
- Analysts can use these identificators to identify uspicious activity and refine their tools.
  - Analyzing activity reveals more indicators (indicator lifecycle)
  - Indicators must be managed and validated to ensure that they are relevant to the monitored threats.

- Kill chain (Intrusion stages from planning to executing objectives within a targeted system)
  - Reconnassaince (Identify and choose targets)
  - Weaponization (the automated weapon / payload is created)
  - Delivery (The payload is sent to the targeted system)
  - Exploitation (The intruders code is triggered in the victim host)
  - Installation (Installation of a trojan or backdoor allows access to victim's system and environment)
  - Command and Control (a channel to an external server is established to control system manually)
  - Action on Objectives (Attackers can do their things eg. data theft, alter data or infiltrate further the network.)

- Six defense actions from Department of defense (Dod) - detect, deny, disrupt, degrade, deceive, destroy to be used with the chain
  - Defenders can can detect and mitigate even new vulnerabilities by investigating repeated indicators (patterns in tools or infra used in other phases of the attack etc.)
  - Resilience can be measured (eg. detection and mitigation rates)
 
**Darknet Diaries**
EP 136: Team Xecuter 
Source: https://darknetdiaries.com/transcript/136/
2 stories 

Story 1

Before steam marketplace all games were all over the internet
- Risk of to become scammed with game purchase (mallware, pirated game, knock-off etc.)
- Three step-process to publish and sell a game on Steam: 1) submit  a steam page, 2) Submit a game for review (by Steam, 3) publish if the game was approved
An attempt to publish a game on Steam without the process
- tricked the process submitting answer that the game was published in a dorp-down list that asked the stage that game was in. People were able to download the game for a whole day before Steam noticed and took the game down.

Story 2

A website admin (Gary) for a website forum talking about hacking video game consoles got to jail for 40 months and owes $10 million to Nintendo + $4,5 million in restitution
- They did not sell any pirated software on the forum but they adverted mod devices for example Playstation and Nintendo mini consoles and a device to hack Nintendo Switch console and had a link to the page you could buy them from.
- The person that (MAXiMiLiEN) had hired Gary to moderate site was selling these mod devices
   - He charged 25 $ for pirated switch hacking software 
   - He got sentenced in several countries to pay huge compensations for copyright crimes but he stays in his home country France where the court decided not to judge him.
 - The moderator (Gary) got arrested while living in Dominican Republic during Covid lock (reason is not clear)
 - He was then sent to Canada but the plane landed in New Jersey for refuel and people's passports were scanned
   - Gary had a lawsuit from Nintendo and he was arrested
   - The lawsuit was for intellectual property infringement
   - Nintendo calculated that a person with a modded system buys 2.41 less games and they multiplied the estimated amount of licences 500.000 with the value of a game $59.99 = $72 million which was rounded to $10 million which is the max sum for a civic lawsuits in Washington state
   - Also the judge wanted to make him a warning example and sentenced him to jail for 40 months + that $14,5 million
- The guy who was selling the chips is living a luxurious life in France (FBI lookng for him) but cannot do anything when he stays in France.

**ATT&CK Enterprise Matrix**
MITRE ATT&CK is a collection of tactics, techniques and procedures that APTs use against enterprise networks
Definitions and examples: 

Tactic = Tactics explain why an attacker uses certain methods. 
  - Eg. To get and maintain an access to a system (Persistence).
  - Eg. To steal or transfer data from victim's system (Exfiltration).
    
Technique = Explains how attackers achieve their goal.
  - Eg. Run scheduled code to stay persistent in a system or moving data (Scheduled task)
  - Eg. Prepare data for exfiltration by staging the collected data in a specific location (Data staging)
    
Procedure = The real-world implementation used by attackers
  - Eg. Schedule a malicious cron job (a scheduled automated task) to maintain access in the system.
  - Eg. Use a PowerShell script to stage and transfer data to a Google Drive or other cloud account they control. 


## a) How would you compare Cyber Kill Chain and ATT&CK Enterprise matrix? Who do you think could benefit from these models?

Sources: https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html, https://attack.mitre.org/resources/faq/

Cyber Kill Chain and ATT&CK Enterprise matrix are both cyberattack frameworks which complement each other.
- Cyber Kill Chain focuses on ordered high-level stages of an attack to understand its structure to prevent and stop them as early as possible.
- For organizations to understand and prevent, detect and stop attacks early.
- ATT$CK is a detailed framework and focuses on the actions of attackers
- Unordered tactics that may not all happen in a same attack
- For roles that are deeply focused on security (security teams, threat hunters, security engineers etc.)

## b) Pick a security incident and learn about it. Write briefly about it. Point out the concepts of threat actor, exploit, vulnerability and (business) impact. (You can find writeups about security incidents from Darknet Diaries and Krebs)
Crooks Steal Phone, SMS Records for Nearly All AT&T Customers

Source: (https://krebsonsecurity.com/2024/07/hackers-steal-phone-sms-records-for-nearly-all-att-customers/)

- Attackers got an access to a third party cloud platform (Snowflake) and got access and downloaded AT&T customer call and text interactions between 5.1.-10.31.2022 and 2.1.2023.
- The data did not include any sensitive customer data like social security numbers or content of messages but phone numbers and location information where the call had been made.
    
- Threat actor: At least one person arrested but probably more hackers were involved
- Potential exploits used: Credential stuffing (stolen username-password combinations), Brute force Attacks (automated tools to try common passwords), 
- Vulnerability: Weak protection on Snowflake cloud accounts containing customer information that rely only on basic usernames and passwords
- AT&T reported that there should not be financial impacts on this incident but still there could be several consequences to its brand and customer relationships.
  - Possible business impacts: financial and reputational damage, loss of customer trust, customers could also file a lawsuit against AT&T. Reputational impacts also for Snowflake and maybe other business partners 
    
- Also other companies that used Snowflake cloud platform to store customer data have been reported similar cases with stolen customer data.
  - Eg. Advance Auto Parts stolen data included full names, SSNs, driver licenses and government ID numbers of all employees and job applicants.

## c) Install Debian on Virtualbox. Report your work, including the environment (including host OS, the real physical computer used), the steps you took and their results.

Host OS: Windows 10 Pro
CPU: Intel Core i7-7820HQ CPU@2.90GHz
RAM: 16 GB
System 64-bit

Installation steps:
1. Download Debian ISO Image
- Go to https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/
- Downloaded debian-live-12.7.0-amd64-xfce.iso

2. Create a New Virtual Machine
- https://cdimage.debian.org/debian-cd/current-live/amd64/iso-hybrid/
- Clicked Windows hosts to start the download (installer file: VirtualBox-7.1.4-165100-Win)
- Ran installer and selected yes to all with default values (Note: Unlike in instructions (https://terokarvinen.com/2021/install-debian-on-virtualbox/), there was no Expert install option during the installation)
- Ran VB and selected Expert Mode from Tools
- Clicked New from the tool bar
- Name and Operating System
  - Name: DebianTeroKarvinenCom
  - Folder: Default value in C:\Users\XXX\VirtualBox VMs
  - ISO Image: C:\Users\XXX\Downloads\debian-live-12.7.0-amd64-xfce.iso
  - Type: Linux
  - Subtype: Debian
  - Version: Debian (64-bit)
  - Selected 'Skip Unattened Installation'
- Hardware:
  - Base Memory: 6000 MB
  - Processors: 1 CPU
- Hard Disk
  - Selected Create a Virtual Hard isk Now
  - Hard Disk File Location: C:\Users\XXX\VirtualBox VMs\DebianTeroKarvinenCom\DebianTeroKarvinenCom.vdi
  - Size: 60 GB
  - Hard Disk File Type and Variant: VDI (VirtualBox Disk Image) (default)
  - 



