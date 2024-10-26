# h1 Adversarial Mindset (homework)

## x) Summaries
**Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains (Hutchins et al 2011)**
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
Before steam marketplace all games were all over the internet
- Risk of to become scammed with game purchase (mallware, pirated game, knock-off etc.)
- Three step-process to publish and sell a game on Steam: 1) submit  a steam page, 2) Submit a game for review (by Steam, 3) publish if the game was approved
An attempt to publish a game on Steam without the process
- tricked the process submitting answer that the game was published in a dorp-down list that asked the stage that game was in. People were able to download the game for a whole day before Steam noticed and took the game down.

Gary Bowser
- started career to keep old machines alive after video game crash 1984 by creating devices and software fo Texas Instruments computer
- After Windows game, business started to went down
- Started to make custom PC's and repairing video game systems
- Started swithing to dark side when wanted to investigate and repair consoles
- Console developers did not want people to mod thei systems
  - Hard to fix consoles
  - Game developers also developed anti-piracy things to check if console mod existed

-  Copyright Act. Section 117 says, if you buy software, you have the legal right to make a personal copy of that software. In fact, it’s even essential if you want to do proper archiving of your digital files. So, with early computer games and software, there was no anti-copying methods in place to detect or stop copied games from being played on the computer. That brings us to the Dreamcast.

- They came out with a bios that added new features; it allowed you to put in bigger hard drives, unlock the system. I hated the way you had to modify the system with the wires and everything. My solution at the time — I would actually just take the flash chip off and just reprogram it and solder it back on. Since I was in business before manufacturing hardware, I had the programming equipment and the soldering tools. So, for me, it was quicker just to de-solder the flash chip, reprogram it on my PC, and then solder it back in. I could do that whole operation within less than five minutes, which was a lot quicker than actually opening — sitting there and soldering a bunch of wires in.

- Paul made another mod for the Xbox, this time calling it the Xecuter. He liked that name so much that he started calling his little group Team Xecuter, which is an important part of this story. It’s the title of the episode, right? So, even though he was threatened with legal action to stop producing the PS2 mod chips, it didn’t stop him from making new Xbox mod chips and publishing them under the name Team Xecuter. Now, the courts didn’t think all this modding was cool like I do. In 1998, the Digital Millennium Copyright Act, DMCA, was established, creating a whole new set of rules for copyright infringement in the digital age. Specifically, there were clauses that talked about circumvention. The DMCA criminalized the act of circumventing access controls, which is what video game makers were pointing out when trying to take down these mod chip makers. They were saying, look, you’re going through great lengths to circumvent our anti-piracy controls. That’s a DMCA violation. Video game makers were taking their cases to court and winning them.

- Tony Chen, the head of security for Xbox.
TONY:	When I first joined Xbox, a lot of people throughout Microsoft — I have to explain to them why the problem we’re facing is fundamentally different than the problem that Windows needs to solve for its security. So, on a Windows PC system, the PC owner is the good guy. He’s working with us to prevent his PC from being attacked. The bad guys are the guys out on the internet trying to compromise his PC. So, Microsoft, as a operating system vendor, is working with the PC owner to fight the bad guys out on the internet. Okay, on the Xbox, the owner is the attacker, although the majority of our customers are good, but you have to treat them as the attacker in terms of designing your hardware.

34:45
- GARY:	I was more popular — originally on Xboxhacker BBS, I was a very popular poster on there. I started then posting on Xbox-Scene, posting news for the administrators on there, and then on another site for the PlayStation — it was called PSX-Scene — I was a very popular poster on there, and I started working with the administrator at that site. I was there when geohot — if you remember George Hotz, he found the original — what they called a root key for the PlayStation 3. He posted it publicly on PSX-Scene, and that caused that site to just take off, skyrocket, go from 100,000 users per day to a million users per day. There was lawsuits involved. By the time that happened, I was actually hosting that website for the administrator, and then Sony cracked down hard. They went after geohot; there was court orders. I started posting all of what was happening in the court case. There was actually, at one time, a movie deal being worked. People thought that George Holt would fight Sony, go all the way, and unfortunately, he decided to settle and that was the end of it.

**ATT&CK Enterprise Matrix**
Explain "tactic", "technique" and "procedure" in context of ATT&CK, and give an example of each. 
Definitions and examples: 
Tactic
Technique
Procedure

## a) How would you compare Cyber Kill Chain and ATT&CK Enterprise matrix? Who do you think could benefit from these models?

## b) Pick a security incident and learn about it. Write briefly about it. Point out the concepts of threat actor, exploit, vulnerability and (business) impact. (You can find writeups about security incidents from Darknet Diaries and Krebs)

## c) Install Debian on Virtualbox. Report your work, including the environment (including host OS, the real physical computer used), the steps you took and their results.
