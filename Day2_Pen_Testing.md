# PenTesting

Pentesting is a method for gaining assurance in the security of an IT system. this is done by attempting to breack some or all of the system's security, using the same tools and techniques a hacker might. Sometimes, this is done via a third party tester, which cna help to simulate a attack by limiting usage of internal knowledge or to have a "fresh pair of eyes" to look at the system.


## Cybersecurity Colours

- "Blue Team": Dthe defenders, reponsible for implementing defensive security, damage control, and incidence response. Also often do things such as compliance testing

- "Red Team": Breakers/Attackers. Commisioned tro perform "ethical hacking" of an organisation.

- "White Team": Admins. Responsible for refereeing an engagement between mock attackers and defenders of their enterprise's use of IT systems.

-"Yellow Team" : the builders. The team responsible for developing the security system of an organisation.


The word hacker, while it has negative connotations in common usage, is in fact a neutral phrase, and "hackers" are now classed into various groupings:

- Baclk Hat Hackers - Attackers that generally operate outside of legal boundaries. Motivations range from financial to political or ideological goals.

- White Hat Hackers - Experts that use hacking in ways designed to aid defence, for example penetration testing. Ethical hackers generally fall under this category. Attacks are carried otu with permission from the target

- Grey Hat Hackers - attacks are performed without permission from the owner, but the aim is to then inform the owner of the vulnerability, rather than exploit the vulnerability to steal data or force a ransom, for example.

Types of Testing

Whitebox Testing - testing with internal knowledge of the system

Blackbox Testing - Testing without knowledge of the system. Sometimes this can yield more results than whitebox testing because a lack of knowledge will cause an attacker to try out every possible avenue, which a whitebox test might reject based on believing a part of the system to be impenentrable

Greybox Testing - A test performed wtih some fo the system information revealed


### PenTesters

Can be internal employees or a third party penetration tester. Whne using a third party, it is important to ensure that the third party is trustworthy.

Penetration tests can, by their nature, not be entirely procedural, as it is impossible to simply draw up a full list of test cases. Quality of pentesting therefore strongly linked to the abilities of the pentesters

MCSC recommends that governement organisations use testers and compnaies which are part of their CHECK scheme. NGOs should use teams qualified via one of their schemes, such as the Cyber Scheme or TIGER scheme


### Objectives of a PenTest

Objective shoudl be to gain assurance of security setup and management protocols. Should od pentesting to make sure that there are no vulnerabilities or other problems in the system, not performed everytime a new feature is added (there should be processes in place to test new features for security weaknesses, with pentesting serving as a sort of audit of the overall system).

It may also be done via scenario-driven testing aimed to identify vulnerabilities. An example of this might be to simulate an employee losing their laptop and seeing how much access to company systems can be gained this way.

Can gain confidence  that:

The products and security controls have been tested and oconfigured in accorance with good practice

There are no publicly known vulnerabilities or exploits at the time of testing.

## Results of a Pentest

can find out the level of technical risk caused by software and hardware vulnerabilities

- Exactly what techniques are sued, targets allow, and how much knowledge of the system is given to testers beforehand and how much knowledge of the test is given to system adminisators can vayr within the same test regime.

## PenTesting Expiry

Pentesting provides mostly a snapshot of the state of a security system, and is usually done periodically (for example annually). If this is the only means of validating security, then vulnerabilities that may be discovered in the interim can remain unadressed for a long period of time. There is no way to guarantee the security of a system for a set period of time (a vulnerability might bew discovered an exploited the day after pentesting concludes)


### PenTesting Startup Point

- External Network Penetration Test: the PenTester attempts to break into a particular network remotely from a different network.

Internal Nertwork penetration Test - Simulates either the actions a hacker might take once inside or those of an inside threat


### Methods and Targets

- Physical PenTesting: Testing of physical access poitns, e.g. testign if access cards to the building can be cloned, or access can be gained in another way.

- Social Engineering: Test if employees can be lured into giving access to sensitive information. Seeing what information can be obtained by manipulating human factors (e.g. calling employees askign for passwords, phishing emails, etc.)

- Web Application Penetration Testing: look for vulnerabilities that may be the consequences of errors in software development. Examples include being able to reset multifactor authentication without customer knowledge.

- Client Side Penetration Testing: Look for vulnerabilities in client-side programs that may be able to maliciously interact with company systems. for example, a vulnerability in a browser, or software that might be running on a client machine.

- Cloud penetration testing: Attempt to compromise cloud resources. Important to notify cloud provider in order to avoid incidents and to make sure that no cloud provider rules are breached.


### "Blindeness Level"

- Targeted (Blindless) Penetration Testing: Both teams keep each other informed of their movements. Generally a training exercise on how to respond to a particular attack

- Blind PenTesting: PenTester may be given only the name of the enterprise, and told to find a way to penetrate the enterprise. No information from or contact with security team of the enterprise.

- Double Blind PenTesting: Security Team doesn't get notified that pentestign is occuring. Pentester doesn't communicate with security team. Neither have nay information about the other. Strong way of testing day-to-day security, as security team would not be lookign for attacks any more than usual.

### PenTesting Phases

Similar to Cyber Kill Chain

1. Pre-Engagement Interactions. Meet with client, outline parameters of pentesting. Establish "ground rules". Clear any legal implications.

2. Reconnaissance: Gather information on target org.

3. Scanning: Also known as inspection. Come into contact with the target, searchign for open ports, runnign systems, etc.

4. Threat Modelling: tester identifies the target, maps attack vector. Employs infor gatehred during previous steps.

5. Exploitation: Exploit vulnerabilities that were spotted, see how far an attack can be taken.

6. Foothold Installation: Once access is gained, attempt to establish foothold in system.

7. Analysis and reporting: Include everythign that was done and describe level of access gained. Include analysis on how this could have been prevented.

8. Clean-Up and Remediation: similar to retreat phase from cyber kill chain. 

Tools

A wide range employed, will be testign a few of these out later.



## Reconnaisance and Footprinting

Footprinting: the process of collecting as much info as possible about the target system, with the goal of finding avenues to epentrate the system. this is analogous to the reconnaisance stage of the previously discussed cyber kill chain. Also keepign track of changes to the profile of the organisation, e.g. if employees have recently joined, or are leaving/looking for other work.

#### This helps to:

Know security posture: details about security and management protocols, configurations or presence of a firewall. Information about what the company has or does for protection.

In terms of eventual outcome, allows a reduction in potential attack area as part of reporting or analysis.

Identify vulnerabilities; for example if software is beign used with a publicised vulnerability. usually, this involves listing as many of the techniques or programs used by the organisations, and then researching each of them for vulnerabilities.

Draw up a network map: this helps the attacker to understand the system structure and search for ideal entry points. When pentesting, it helps identify likely targets.

Techniques used in reconnaisance are listed under "open-source intelligence" OS-INT represents the surface web, as well as other components (termed deep web and dark web). Filtering relevant information to get the parts that are relevant to a particular organisation is particulalrly importnant

Deep Web:
Poriton of the web where there is no indexing, makign it unsuitable for regular search engine usage. contains a lot of records and databases, which are usually hidden behind logins, subscriptions or similar. Information here usually requires a login to a particular database in order to be able to access files. These are accessible, but not  accessible to the general public.
Some pages are part of the deep web because they don't use a common top-level domain (e.g. .co.uk, .gov, and so on), meaning they are not indexed directly in a search engine. Many deep web sites are stored in databases supporting everyday browsing activity, such as banking, social media, or health records.


Dark Web:
Even less accessible than the deep web. Relies on connections made between trusted peers, and requires specialised tools to access. the best known of these is TOR and the second is I2P. Has something of a reputation, usually connected to illegal activity, such as drug trafficking. However, there are also positive sides to the relative anonymity afforded by the dark web, meaning that activists or whistleblowers may be able to act here without repercussions


In terms of usefulness to a pentest, it can be the case that data stolen from a company may be available here.

OSINT Use case

Civilians may use it for basic knowledge, business, or public opinions

Governments might look for threats to national security

CyberSec professionals may use it for:

- Cyber Defence: for exampel looking for user information so that compromised users may be found, or details of a particular network which might indicate an attack is being planned or a particular aspect is compromised

Pentesters: reconnaisance on a target

Security analysts - similar reasons

Cybercriminals - for research on victims, or to obtain information if it is available for sale.

OSINT tools ar elossely categorised under
- domain and IP search
- Exposed data on enterprise website
- exposed data already on internet
- hidden data in files
- connected device searches

A few example tools:

WHOIS:gives addtional information about a domain. Cna also use domaintools, icann, WHOIS Search, CEntralOps, and other tools.


Can also use DNSrecon, a python sdcript that obtains information associated with a DNS address.

Finding additional domains increases the potential attack surface, as more obscure domains may be less well protected and therefore easier to attack.

Google Hacking/"Dorking"

Use advanced search operators to search mroe deeply than a normal google search. this can help obtain information that might not be normally accessible, including for example searching in not normally accessible databases. for example to search with a particular subdomain, use site:[domain name, e.g. .edu],

## Harvester

Finding information on employees can be useful. The easiest way to find this can be LinkedIn,  colelcting profiles on interesting people and maybe even searchign their personal social media. The harvester helps with finding the email address associated with an account, which in turn allows phishing attempts.

## Intrusion Information System

DShield is an example of this. Provides a platform for users of firewalls to share intrusion information. Can find information about certain firewalls here.

virustotal: database of virus information. Can upload files and scan files for viruses using different scanning methods.


#### Document searching
Fingerprinting Organisations Collected Archives (FOCA): available via github. Idea is that it is a tool used mianly to find metadata and hidden information in a document that it is scanning.

Metagoofil allows extracting of metadata from files, and is able to generate a report on the findings. Cna give the tool a target website and target filetypes to obtain extracted metadata.

### Shodan

Allows searching for an internet connected device. Keeps scanning certain servers attempting to connect to devices that it finds. Particularly famous for finding things such as unprotected webcams or unprotected industrial control systems. Not a free service, but trial is available. Can use to find a specific device. Can also search IP addresses, to find out what IP addresses are connected to a particular network.

#### Wappalyzer

Firefox plugin that identifies technologies used on a website for various purposes, e.g. analytics tools, libraries used, and so on. This can be very useful as soem libararies or tools may be prone to a particular exploit.


### crt.sh
All SSL certificates are released for public inspection. Can search for certificates associated with a particular domain, including a log of all the certificates that hav ebeen issued. Cna also report problems with a certificate to the certificate authority.

### Sublist3r

Used to enumerate the subdomains associated with a domain.

### Wayback Machine

Get snapshots from a past iteration of a site, for example to obtain information that may have been accidentally exposed in the past

### OSINT Framework

a directory allowing the lookup of for example company email addresses. very powerful tool if the correct search terms can be used to filter the results.



In conclusion,there are a lot of potential avenues of attack, and choosing a viable one is a difficult part of penetration testing.


