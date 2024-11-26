# h5 HelSec

## x) Watch and summarize. Add your own comments, ideas and questions.
Two full length HelSec presentations on the November event (2024-11-21 w47 Thu)
Voluntary bonus: A third one.

18:00 - [Starting words]

## 18:15 - Jos Helmich - Industrial Cyber Security

Sources: _https://www.enisa.europa.eu/, https://single-market-economy.ec.europa.eu/sectors/electrical-and-electronic-engineering-industries-eei/radio-equipment-directive-red_en, Chat GPT:"compare the leavel of cybersecurity acts  EU vs US", https://www.paloaltonetworks.com/cyberpedia/what-is-ot-security, CHAT GPT: "what is the difference in office cloud and industry cloud", https://www.europarl.europa.eu/topics/en/article/20230601STO93804/eu-ai-act-first-regulation-on-artificial-intelligence#ai-act-different-rules-for-different-risk-levels-0_

Product security architect in KC cybersecuiry team
Member in ENISA advisory group

Here today because of Hero's Quest pc game 
  - I have this game complete in box. :) 

Working on embedded devices in KC 
- Brake monitoring unit
- Remote operation station
- Electronic Crane Unit

ENISA (European Union Agency for Cyber Security)
- Allocation of Funds
- Strategic Questions
- Review Threat Horizon 2030
- Write papers
  - Cyber Security Act
    - Cybersecurity certification schemes to define standards for products, processes and services
    - To provide security confidence
  - NIS  (basic security requirements)/ NIS-2 (stricter requirements and supervision)
 
Advisory group makes suggestions to EU parliament 

Industrial EU Directives
- Machines Directive
- RED - Radio Equipment
  - A regulatory framework for radio equipment on the market (personal data, safety and health, etc.)
General EU Laws & Directives
- GDPR - General Directive Data Protection 
- NIS-2
  - Rules and guidelines to mange and mitigate security risks
  - A national authority in every EU state to oversee the implementation of the directive
- CRA

US legislative mumbo jumbo maybe not to stay because can be changed by the goverment
  - I asked ChatGPT about differences between cybersecurity acts in EU and US:
    - EU:
      - Centralized supervision, all EU member states must
      - Broader coverage
      - Mandatory incident reporting, significant sanctions 
    - US:
      - Supervision decentralized to different agencies and state specific laws
      - More caps in coverage in different sectors
      - Voluntary incident reporting, sanctions by sector
   
Supplier to the US goverment must fill a CISA attestation form
- Strict form
- NIS-2
  - Large impact on organizations cybersecurity requirements
- NIS-2 in Manufacturing
  - IT Security 
  - OT Security (Operational technology: Hardware and software to control and monitor industrial equiment and processes)

Office Cloud and Industrial cloud
- Office environments are protected by a firewall
  - Office workers and general office products
  - business critical data, secure general data
- Industrial network is protected by two firewalls (both office and industrial clouds)
  - Tailored for specific industries (healthcare, manufacturing, finance etc.)
  - Secure operational data, indstrial workflows, information from systems
  - Real-time security critical to prevent operational problems
  - Industrial zone has no connection to internet - In real life does not happen because need to have   VPN

NIS-2 vs CRA
NIS is aout your organization
CRA is about messing up someone else

Need a certiciable standard for both to address the CRA

NIS-2 supply chain consequences
Questions to supplier:
- What is the minimal password length

CRA supply chain consequences
- Questions from the customer

62443 family requirements for industrial cybersecurity

Security Levels
1. Accidental tourist (accidentally finds something from internet eg)
2. Normal users 
3. Hackers
4. Nation state (against hostile nations, terrorists etc.)

EU legislations for AI - New Legislative Network
- Product safety requirements
- Data requirements - GDPR
- Cyber Resilience Act
High risk for fundamental freedom
- Unacceptable risk (some exceptions can be made E.g. law enforcement use)
  - a threat to people (manipulous activity, eg. racism, dangerous behaviour to kids)
  - Social scoring
  - Biometrical identification and categorization of people
  - Biometric identification systems (E.g. facial recognition)
- High risk - your privacy (Systems need to be assessed throughout their life-cycle)
  - AI systems that do not fill EU's product safety legislation
  - AI systems that need to be registered in an EU database
- AI with specific transparency obligations (E.g. Chat GPT)
  - Non high-risk systems
  - People must be aware which is AI generated (clear label needed)
  - Building the system to prevent from illegal content

Standards
- ISO/IEC 42001:2023
- ENISA - Multilayer network for good cs practices for AI
- ETSI - Secure Artificial Intelligence Technical committee
- NIST - NAtional Institute of Standards and Technology

- Standards protect companies from legal consequences

## 19:20 - Heikki ”zokol” Juva - State of Union
Sources: _https://single-market-economy.ec.europa.eu/sectors/electrical-and-electronic-engineering-industries-eei/radio-equipment-directive-red_en, https://kyberturvallisuuskeskus.fi/fi/toimintamme/saantely-ja-valvonta/kyberkestavyyssaados-cyber-resilience-act-cra, https://www.ssl.com/blogs/what-is-certificate-pinning/_

Bought 10.000 worth of electronic consumer things and measured how they apply the regulations


**Two regulation projects**

RED (Radio Equipment Directive) 
  - 18031 (Cybersecurity standards for the radio equipment)
  - Reqs for health, safety, electromagnetic compatibility, and efficient use of the radio frequency spectrum
CRA (Cyber Resilience Act)
  - Setting minimum standards of CS to systems of products that can be connected with another product or a network. 
  - Technical security reqs
  - Vulnerability handling reqs

- 11/2019 Launch of the Traficom IoT Cybersecurity label
- 1/2022 RED standard work starts
- Q2 2024 CRA standard work starts
- 12/2024 CRA effective
- 8/2025 RED is enforced
- 9/2026 CRA vulnerability notification starts (21 month transition period from CRA law effective)
- 12/2027 CRA is enforced (36 month transition period from CRA law effective) 

**Testing**

Questions
How do devices communicate?
Devices under testing
- Consumer market
- Connected to internet
- Popular devices

Blackbox testing

Device Classification
- Device is connected to network?
- -> RED- part 1 applies
- Does the device collect personal info?
- -> RED part 2 applies

Good requirements
- Vulnerability coordination (Vulncoord e-service)
  - Forces companies to establish vulnerability coordination and reporting to a centralized authority
  - Target: to ensure that vulnerability info, patches and updates reaches everyone 
- Inputs are validated
- Proper cryptography
- Good passwords
- Content filtering; digital content loaded only from trusted sources (applies to RED part 2)

Some requirements have problems in real life
- Compatibility causes problems
  - Less security if the device needs to be E.g. backwards compatible
  - Outsourcing security; Data exposure, complience challenges, loss of control, different laws with data transfer etc.(Source: Chat GPT 'what problems there are in outsourcing cyber security')
  - Paper-based evaluation; All reqs proven by only documentation but not the device in practice
Example:
- Company Eagle make IP cameras
-  E.g. child movement monitoring
  - Sends all collected info to a cloud
  - RED part 1 & part 2 classes (Internet connected and gathers personal info) 
-  EagleSock - A smart sock that monitors heartrate and saturation etc.

Test results: 

RED part 1
- Software updates are enforced
- Opened device (Is the device storage secure?)
  - Unencrypted files that are not signed
- No known non-mitigated exploitable vulnerabilities?
- 1107 security issues found
- Password are unique or strong?
  - No (Admin 12345)

RED part 2
- All sensors that may affect user's privacy are documented? - OK
  - Clips are saved
- User notified - letting know that info is saved - No
- 3rd party information
  - Gathers a lot of info about you and child, names, health info
- Bypasses GDPR
  - Should read the legal texts - Not in force in EU
- Deleting all info possible?
  - All data can be deleted, but no one knows if the data is really deletd from the cloud. 
  - Was still able to find users information (E.g. wifi) from the device after wiping the information and restoring factory settings.

- How do consumers devices communicate
  - Communication mostly to Western countries
  - Most devices use Amazon AWS
  - Most of the data is encrypted though
  - Transport Layer Security (TLS) version 1.3 used only little amount 1.2
  - 90 % use TLS and CERT pinning
    -  Certificate pinning is a security mechanism ensures that the client communicates with a trusted server.  
  - 80 % implemeted on baremetal - (no OS) - automatic tools cannot hack
  - 66 & use wifi for communication
  - 90 % are online only temporarily - battery operated devices - only communicate with device when used
  - Hard to hack because not connected all the time but only for a few seconds time to time

Common issues
- Data is not deleted even if asked / Or at least cannot be sure that it is deleted
- Sharing info with 3rd parties
- Complex manufacturing process, even the seller does not know how their device works

Attribution
- Finding the actual manufacturer by dumbing firmware
- googled the prefix and found the company

The quality of cryptography was a very good quality (A happy suprise!)

Man in the middle attack does not work with common tools
