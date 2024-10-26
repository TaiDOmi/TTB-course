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

- PlaStation classic mini - USB- memory with games
- Nintendo mini with a cartridge adapter available
- Amazon listes usb stick sales address for 15.000 pirated games
- MAximilian 

- His developer got to work building two physical devices; one that would slide into the Joy-Con port and trigger the glitch, while the other would go into the USB drive to have the system boot into a custom firmware. Team Xecuter called this add-on the SX Pro. The idea is that it enabled you to copy games that you already had or play any pirated games that you had. The design was clean and super simple. People who had no experience modding systems could easily get this working and were giving it great reviews. So, they had this thing all developed and manufactured, and then they wanted to announce it on the forum that Gary was the mod for, and this is where Gary was obligated to promote this device, since that was the deal that he made with MAXiMiLiEN. Now, when you’re a mod-maker, you’ve got some potential things that can go wrong with your whole business. See, sometimes Team Xecuter would sell their products for, let’s say $30, but then see the exact same product being sold directly out of Asia for $2. It was pirate versus pirate, because the factory that was making the chips for Team Xecuter would just sometimes make some extra and sell them directly to the consumer, totally undercutting Team Xecuter. So, Max didn’t want that happening with SX Pro, so he decided he was going to add his own software into the thing.

- License for pirated software 25 $ to protect from asia copys
- People were mad to pa from pirated software
- The other thing that people were getting mad about is that some users were reporting that their Switch would become broken after using the SX Pro. Yeah, they were, because what Max did here is that he didn’t want someone else trying to understand or steal the software on the SX Pro.

- Made also Nintendo mad
- You’re making money from our hard work? We’ve gotta stop this. So, first they patched it. All Switches made after 2019 were no longer vulnerable to this attack, and then they started trying to find and stop this whole Team Xecuter operation. So, uberchips.com was another place you could…

GARY:	That was one of the resellers in the United States that got sued by Nintendo for selling the device. They were one of the first resellers that were gonna be selling the SX Light and the SX Core for the Switch.

- PR guy - modifier for a site that adverted modding products and had links to sites
- JACK:	Hm, no pirated games on these forums were allowed. I’m trying to think; so, Team Xecuter wasn’t actually selling anything on the site. They’d just link to places like Divineo where you could buy it from. But still, the Team Xecuter stuff mostly enabled your device to be able to play pirated games and didn’t actually have pirated games on them, except for one device. Yeah, but the — okay, but the True Blue is stick-full of pirated games.
- I mean, we didn’t sell the devices on the Maxconsole website. We talked about it. It was up to you to find the devices. I didn’t profit off of it, either, so…
- GARY:	Not really. I mean, people come up with estimates and stuff. Nintendo themselves came out with an estimate; they estimated around 500,000 SX OS licenses were sold at the time. So, you could think of 500,000 times $25 for the license fee, and that’s not on the hardware; that’s just on pure profit. So, that’s not counting the Gateway 3DS or any edit devices.
- Airports were gonna reopen, you’ll be able to go outside all day long, the bars will be open again, the beaches will be open again. It was gonna be the end of the extreme lockdown. So, I was looking forward to it. But 5:00 in the morning, instead of waking up at 7:00 in the morning and going outside and enjoying outside, [MUSIC] 5:00 in the morning, I woke up with a shotgun pointed to my head and a bunch of people in my place. At first I thought I was getting robbed. I didn’t know what was going on. There was a lot of crime during Covid. All I knew is I’m getting dragged out of my house early in the morning and there’s a bunch of people in the place looking at all my electronics, grabbing all the computers. I tried to talk to them to find out what’s happening. They refused to talk to me in English or Spanish and acted as if I were speaking Russian or German, looking at each item and — oh, what’s this guy talking…? Even though one girl that I knew lived above me came downstairs, they even didn’t tell her what’s going on. They were just saying, oh, he’s being taken to have his papers checked and once his papers get checked, we’ll release him. So, they took me out of there, brought me to the Interpol office. I sat down on a couch. They still continued to refuse to talk to me. I was screaming that I wanted to talk to the Canadian government.

- After about a day of just sitting on the couch, the next day on the 28th, they drove me to this cage in the middle of nowheres with a bunch of other patients that they had rounded up, and threw me in there. I spent like, two or three days in that cage, still not knowing what’s going on. Luckily, I got a little bit of food from someone else that got food brought to them, another Haitian, an old guy that took pity on me. He gave me some of his food, shared it with me. ‘Cause in the Dominican Republic, when you go to jail, you don’t get fed. Your family has to show up and bring you food. Otherwise you just starve. So, I spent three days like that. Come October 1, they take me out of the cage and they said, we’re taking you to see the Canadian government. Finally; about time someone listened to me. But instead, they drive me to the airport. I start yelling and screaming at the airport again, saying, hey, where is the Canadian government? Well, they can’t make it. You can find out when you get back home. They handed me my passport, they handed me 3,000 pesos, they handed me a plane ticket to Toronto, and they said, once you’re on the plane, you get to Canada, you can figure it out. You have to leave the country. I said, well, am I under arrest? They said, no, you’re not under arrest.
You’re just being kicked out of the country. Your Visa is expired. You’re not welcome anymore in the country. I was like, well, I want to talk to the Canadian government. They said, no, you can talk to them when you land. So, I got on the plane. It was one of the first airplanes after the Covid lockdowns ended, so it was just packed with people. There was an unbelievable amount of people on the plane. It flies and gets to New Jersey, and it has to land in New Jersey, refuel again, and then it would take back off and go to Toronto. But after 9/11, any time an airplane lands in America, everybody has to get off, scan their passport before they can get back on the airplane. Before 9/11 you would just sit in the terminal in what they call a transit area. You didn’t actually enter the country. Of course, the moment I scan my passport in New Jersey, that’s when the indictment showed up and I got taken to secondary inspection. From there, I was told I was actually gonna be arrested. They drove me to the Essex County Jail which was a nearby jail. The FBI drove me there. They said, you’re gonna stay here overnight and then we’re gonna take you to where your case is. I still don’t know what I’m being arrested for or what — anything about. October 2nd came. I got read my rights by a judge over the telephone when I was in county jail, and that’s when I found out I had thirteen different charges on me with money laundering, wire fraud, and bypassing technology measures and all that.
- JACK:	They take him to jail. He stays there for five weeks. They take him to another jail; he stays there for three weeks. He finally sees the judge and they ask him, hey, are you guilty or not, Gary? He’s like, these charges are crazy. I’m not guilty. Now, at this point, the prosecuters have to gather more evidence on him. Gary’s name on Max Console Forum was simply GaryOPA, and that name was easily linked to his company that sold Texas Instrument Parts in 1984. So, it was very easy to figure out who Gary was. He made no attempt at hiding what his real name was. So, when Nintendo wanted to come after Team Xecuter for the SX Pro stuff, they came right after Gary. But he wasn’t the only one caught up in this. Let me read the title to you of the FBI press release. Two members of notorious video game piracy group, Team Xecuter, are in custody. The other that was arrested was MAXiMiLiEN.
- He was arrested while on vacation in Tanzania, but he somehow convinced the police there that his arrest was illegal, and guess what? The Tanzanian police agreed and they let him go. Quickly, he called a friend who had a plane in South Africa, and they flew the plane to him, and he hopped on it and flew back to France. While on the plane, he posted a picture on Instagram saying that he’s flying alone on a ten-person private jet. But when you have to go, you have to go. Apparently he’s untouchable in France by US authorities. The FBI cannot seem to get him arrested or extradited there, but they were able to freeze some of his bank accounts and cryptocurrency accounts that were within the FBI’s reach. There was a third person listed on this indictment, too, a Chinese guy named Chen. My guess is that he was overseeing the production of the chips in China, but since he’s in China, he’s unreachable by the FBI, so he was never detained or arrested. Six months go by for Gary, sitting in a prison in Seattle.
- 
JACK:	Nintendo was trying to sue Gary for intellectual property infringement and wanted him to pay them $10 million in damages.
- How that — comes up with that figure is — going back to Nintendo, their experts testified that they estimated around 500,000 licenses were sold, and their experts testified that their studies show that when a system is hacked, that people buy 2.41 less games. So, there’s, let’s say the top ten games; Zelda, Mario Kart, Super Mario, stuff like that. Well, those top ten games — 2.41 less sales. So, when a system is hacked, someone will buy maybe only seven games or eight games, not the full ten games. So, they take the 500,000 times the 2.41 times the value of the game, $59.99; comes to around $72 million. There is then three people on the indictment; me, the guy in China, and Max, so my share of it, being approximately one-third — let’s just round it off to $10 million, which is usually the max that you can get in Washington state, anyway, for a civic lawsuit.
- JACK:	[MUSIC] So, Gary owes Nintendo ten million bucks. He’s in his fifties now, and his only job he’s ever had for the last twelve years is gone. So, it’s just impossible to pay this back. He’d have to make over $500,000 a year for the rest of his life to pay this off.

- JACK:	This is interesting. So, the FBI went to the — to Sony and said, hey, we caught the guy who was selling pirated video games. You want to be part of this lawsuit? They said, no, we don’t want anything to do with it. That’s really crazy.
GARY:	But they weren’t interested. The PS1 was a failure on their part, anyway. It was being sold for $19.99. It was a disaster.
JACK:	The PS1 Mini.
GARY:	Yeah, the PS1 Mini. So, they were not really interested in flying lawyers down and presenting evidence. The only people that were interested, in the end, was Nintendo and the ESA. They were the only two people that showed up in February for sentencing and victim impact statements.

- JACK:	On top of the forty months, the judge also demanded that he pay $4.5 million in restitution, which adding it all up, he’s gotta pay $14.5 million and spend three years in prison for what he did. I don’t like that the judge said out loud that he wanted to make an example of Gary. Does that kind of thing really work, to pick one guy you caught and give him a brutal punishment just because you can’t catch the other people that were doing it? I don’t know. Based on what I’m hearing here, $10 million is already too much of a punishment for what he did, and now a judge is saying, no, no, no, that’s not enough; you need to pay an extra $4.5 million more and go to prison for three years on top of that. Is this sentence fair or is it cruel? If the judge is saying things like let’s make an example of this guy and gives him more punishment than he deserves, then isn’t that the definition of unusual punishment? Now, Gary is not a US citizen. He’s a Canadian, so theoretically, if he’s not living in the US, he doesn’t have to make payments towards his federal crime. But Nintendo does not want him to slip out of paying them, so they put into the civil case that one, his wages will be garnished. That is, anywhere from 10% to 30% of every paycheck he earns goes automatically to Nintendo, and two, that this is enforceable by law in any country that Nintendo has an office in, which they do have an office in Canada, and three, he cannot declare bankruptcy to have his civil fine removed from his debt. While Gary was in prison, he already started making payments towards all this.
- irst of all, this is a game that’s twenty years old. It was for the GameCube, but people are still really into it. But Nintendo doesn’t like that players are staging tournaments to play Super Smash Bros. Melee, and have sent cease and desist letters and even threatened more legal action unless tournaments get canceled. They think that what they’re doing is protecting their brand, but it’s one of those situations that’s like, cut off your nose to spite your face sort of thing. The more they fight with their own players, the worse their brand gets. One of my favorite childhood memories ever was getting a Nintendo for my birthday and opening it up and playing it with my friends during my whole birthday party. Decades later, I still remember which friends were there at that party, what games we played, who was good at it. Pick any other birthday I had as a kid and I can’t tell you a thing about it, where it was or who was there, but this one I remember because Nintendo brought so much joy to me as a child that day. But now that I’m older, I can see now that Nintendo has a lot of growing to do still.

- A website admin for a website forum talking about hacking video game consoles
- They did not sell any pirated software but they adverted mod devices for example Playstation and Nintendo mini consoles and a device to hack Nintendo Switch console. 
- License for pirated software 25 $ to protect from asia copys



**ATT&CK Enterprise Matrix**
Explain "tactic", "technique" and "procedure" in context of ATT&CK, and give an example of each. 
Definitions and examples: 
Tactic
Technique
Procedure

## a) How would you compare Cyber Kill Chain and ATT&CK Enterprise matrix? Who do you think could benefit from these models?

## b) Pick a security incident and learn about it. Write briefly about it. Point out the concepts of threat actor, exploit, vulnerability and (business) impact. (You can find writeups about security incidents from Darknet Diaries and Krebs)

## c) Install Debian on Virtualbox. Report your work, including the environment (including host OS, the real physical computer used), the steps you took and their results.
