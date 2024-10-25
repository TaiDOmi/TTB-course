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
  - 

**Darknet Diaries**


**ATT&CK Enterprise Matrix**
Explain "tactic", "technique" and "procedure" in context of ATT&CK, and give an example of each. 
Definitions and examples: 
Tactic
Technique
Procedure

## a) How would you compare Cyber Kill Chain and ATT&CK Enterprise matrix? Who do you think could benefit from these models?

## b) Pick a security incident and learn about it. Write briefly about it. Point out the concepts of threat actor, exploit, vulnerability and (business) impact. (You can find writeups about security incidents from Darknet Diaries and Krebs)

## c) Install Debian on Virtualbox. Report your work, including the environment (including host OS, the real physical computer used), the steps you took and their results.
