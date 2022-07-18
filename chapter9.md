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