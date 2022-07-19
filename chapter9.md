# Chapter 9: Network Risk Assessment

## Security Risks

Hacker: originally someone who mastered the inner workings of computer hardware

* white hat hacker: security experts hired to assess risks
* black hat hacker: use skills to bypass security systems to gain information
* gray hat hacker: uses skills to exploit security weaknesses to educate

### People Risks

Many intruders gain access to networks just by asking users for their passwords (pretending to be an IT worker)

Phishing: gaining sensitive information by posing as a person of authority, asking users to submit information through emails and forms that look legit

Tailgating: posing as an authorized employee and following someone into a restricted area

Insider threat: trusted or authorized people who have malicious intent

* background checks for employees and contractors
* employees are only given as much access as is needed to do their job, which is terminated when the person no longer needs it (principle of least privilege)
* checks and balances on employee behavior
* data loss prevention: sensitive information cannot be copied or transmitted

### Technology Risks

Typically require more knowledge than exploiting people risks

Types of attacks:

Spoofing: MAC and IP addresses can be impersonated

Denial of Service: legitimate user is prevented from accessing resources because of an attacker's intervention
Ex: System is flooded with requests so that network can't respond to all of them, disrupting service

DDoS: smae as above, but attacks come from multiple sources (users often unware that their computer is being used)

DRDoS: DDoS attack bounced off uninfected computers before being directed to target

amplified DDRoS: simple requests that trigger large responses from the target

PDoS: damages firmware, "bricks" the target, usually targeted to routers and switches

DNS spoofing: attacker redirects traffic from legitimate websites to phishing websites using altered DNS records

ARP poisoning: alter ARP tables (contributes to other types of attacks)

Man-in-the-middle: transmissions are intercepted

Rogue DHCP server: may allow hackers to access the entire network

Deauth: fraudulent deauthentication message sent to a Wifi access point

FTP bounce

Backdoors

### Malware Risks

Malware: programs designed to harm a system

Types of malware:

Virus: program that replicates itself onto other computers, may damage files or just be annoying

Trojan horse: disguises itself as something useful, but is actually harmful

Worms: programs that travel through files transfers, can carry viruses

Bot: program that runs without human intervention; can be harmful or useful

Ransomware: locks a computer until a ransom is paid

## Security Assessment

Posture assessment: examination of each aspect of a network to determine how it can be compromised

Attack simulations:
* vulnerability scans: to identify vulnerabilities in a network, can be authenticated (using credentials a user might have) or unauthenticated
* penetration testing: attempts to find weak points in a network, then exploit the vulnerabilities
* red/blue team: red team attempts an attack, blue team attempts to defend the network

Scanning tools can provide hackers (and users) with information about the network, data, etc
Nmap: scans a large network and provides information about hosts and ports; open ports are vulnerable to attacks
Nessus: can scan for network information, as well as unencrypted data on hosts
Metasploit: combines scanning and exploit techniques to discover attack routes

Honeypot: decoy system that is purposely vulnerable and filled with sensitive-looking information to lure hackers

## Physical Security

Computer rooms should be locked, with only authorized people having access; key pad, key fob, access badge, proximity card, or biometrics may keep computer rooms secure

For detecting physical intrustions: motion sensors, video surveillance, tamper detection, asset tracking

## Device Hardening

Securing a device from attacks

Security updates/patches: use them

Change default admin credentials on devices during setup
Since some devices are managed using remote connections, use SSH keys in addition to username/password combos

Insecure services and protocols should be disabled when not in use

Hashing: transforming data using an algorithm; not the same as encryption, but can ensure data is not altered in transmission; hashing is part of good encryption protocol
Data can be hashed, sent, and compared to a hashed version of the original data
Passwords are often hashed; even if passwords are compromised, they will not be useable to a hacker

Anti-malware software (virus scanner) is only one part of keeping computers secure; may not be completely reliable on its own

## Security Policy

Identifies goals, risks, levels of authority, responsiblities...specifies how to address security breaches

BYOD policies require information on what is not allowed, restrictions on the networks, device configuration requirements

AUP: acceptable use policy, what can and cannot be done on a network

NDA: non-disclosure agreement

Passwords!
- Change default passwords on new devices and software
- Do not use information about yourself
- do not use words that might appear in a dictionary
- longer passwords are better
- don't write them down
- change every 60 days
- do not reuse passwords 
- use different passwords for different applications
- use a password management software

Privileged User Agreement: addresses specific concerns about privileged access given to admin and certain support staff

Determine rules for anti-malware software; should be centrally distributed and updated, cannot be disabled by users...