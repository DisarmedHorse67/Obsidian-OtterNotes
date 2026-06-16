[Event] = Is an action occurring in a system or network. 
Examples: 
	- A mouse click.
	- Firewall allowing connection.
	- Email sending.
[Incident] = Is an event but with negative consequence. HTB defines it as an event with clear intent to cause harm to a computer system.
Examples:
	- Data theft
	- Funds theft
	- Unauthorized data access
	- Installation and use of malware and remote access tools.

mshta to retrieve a remote HTA file containing a Metasploit stager*****

Stages of Cyber Kill Chain
[Recon] 
	Active recon
		Identify the target and scope of target network
		Locate open ports
		Identify services running on open ports
		Map entire network
	Passive recon
		Information gathering from web sources (Job Ads, Company partners)
		Social media (LinkedIn, Instagram, Facebook)
		Avoid detection all the time

[Weaponize]
	*"The malware to be used for initial access is developed and embedded into some type of exploit or deliverable payload. The sole purpose of this initial stage is to provide remote access to a compromised machine in the target environment, which also has the capability to persist through machine reboots and the ability to deploy additional tools and functionality on demand."

[Delivery]
	This stage is when the payload or exploit is delivered to the victim(s), through various methods like phishing emails, fake websites, phone calls or by physical devices like USB's or other storage tools.

[Exploitation]
	In this stage is when the exploit is triggered and the attacker try to gain access to the system.

[Installation]
	When the attack gets to this stage is because the initial stager is executed and is running on the compromised machine, from here the installation stage can take some paths like:
		**Droppers**: This is a small piece of code designed to install and run some malware on the infected system and disappear without any trace.
		**Backdoors**: This is a type of malware with the purpose of give the attacker continue access even after reboots, this needs to be installed by the attacker during exploitation phase.
		**Rootkits**: This is a type of malware designed to hide from antivirus software and other security tools. 

[Command and Control]
	In this stage the attacker establishes control and remote access over the infected device, and often the attackers do this on layers, so even if one variant of the malware is detected, they keep the access to return to the infected environment.

[Action]
	This is the final stage of the attack, also known as objective of the attack. This objective can be very different depend on what the attacker wants, some may want to exfiltrate confidential data, others wants to get the higher level of access to deploy some malware or ransomware.

Note: Not every attack keeps a straight line over every stage, sometimes the same stage can be repeated multiple times and may not be in the same order.


***The best actions to take to ensure a secure endpoint & EDR are:***
- Disable LLMNR/NetBIOS.
- Implement LAPS (Local Administrator Password Solution) and remove administrative privileges from regular users.
- Disable or configure PowerShell in "ConstrainedLanguage" mode.
- Enable Attack Surface Reduction (ASR) rules if using Microsoft Defender.
- Implement whitelisting. We know this is nearly impossible to implement. Consider at least blocking execution from user-writable folders (Downloads, Desktop, AppData, etc.). These are the locations where exploits and malicious payloads will initially find themselves. Remember to also block script types such as .hta, .vbs, .cmd, .bat, .js, and similar. We need to pay attention to [LOLBin](https://lolbas-project.github.io/) files while implementing whitelisting. Do not overlook them; they are really used in the wild as initial access to bypass whitelisting.
- Utilize host-based firewalls. As a bare minimum, block workstation-to-workstation communication and block outbound traffic to LOLBins.
- Deploy an EDR product. At this point in time, [AMSI](https://learn.microsoft.com/en-us/windows/win32/amsi/how-amsi-helps) provides great visibility into obfuscated scripts for antimalware products to inspect the content before it gets executed. It is highly recommended that we only choose products that integrate with AMSI.

***When an incident occurs, we need to aim for get information like:***
- Date/Time when the incident was reported. Additionally, who detected the incident and/or who reported it?
- How was the incident detected?
- What was the incident? Phishing? System unavailability? etc.
- Assemble a list of impacted systems (if relevant).
- Document who has accessed the impacted systems and what actions have been taken. Make a note of whether this is an ongoing incident or if the suspicious activity has been stopped.
- Physical location, operating systems, IP addresses and hostnames, system owner, system's purpose, current state of the system.
- List of IP addresses, if malware is involved, time and date of detection, type of malware, systems impacted, export of malicious files with forensic information on them (such as hashes, copies of the files, etc.).

***Important questions to answer when an incident occurs
- What is the exploitation impact?
- What are the exploitation requirements?
- Can any business-critical systems be affected by the incident?
- Are there any suggested remediation steps?
- How many systems have been impacted?
- Is the exploit being used in the wild?
- Does the exploit have any worm-like capabilities?