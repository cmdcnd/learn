### Security Assessment Tools  
[Kali Image](https://www.kali.org/get-kali/#kali-installer-images)  
[Manidant Commando](https://github.com/mandiant/commando-vm)  

### EXTERNAL TASKS  
--------------------  
#### TASK: 16.1 – PENETRATION TEST EXTERNAL OPEN-SOURCE META DATA IDENTITY COLLECTION  
This task identifies the entity’s risk exposure to publicly available identity-based metadata pertaining to its users past and present.  This information provides attackers insight to valid usernames, valid email addresses and format, applications in use, and associated users with business function.  Using these collected data points, the attacker can more effectively form password spraying and spear phishing attacks against the target entity [MITRE ATT&CK ID: T1589](https://attack.mitre.org/techniques/T1589/). The Pen Test team will use active and passive reconnaissance techniques to acquire relevant and actionable information where possible.  

* Tools that can be used for this task.  
[SimplyEmail](https://github.com/SimplySecurity/SimplyEmail) - not currently supported tool.  
[FOCA](https://github.com/ElevenPaths/FOCA)  
[theHarvester](https://github.com/laramies/theHarvester) - built-in to Kali.  


#### TASK: 16.2 – PENETRATION TEST EXTERNAL SPEAR PHISHING ATTEMPT  
This task assesses the entity’s ability to react to a simulated threat actor directed spear phishing campaign derived from data collected via public/open sources only.  

* Tools that can be used for this task.  
[Attack simulation training M365](https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/attack-simulation-training?view=o365-worldwide)  

#### TASK: 16.3 – PENETRATION TEST EXTERNAL PASSWORD GUESSING ACTIVITIES  
This task simulates a threat actor’s ability to derive logon credentials while external to the entity network using brute force techniques [MITRE ATT&CK ID T1110](https://attack.mitre.org/techniques/T1110/) including password spraying and password guessing. This process can include informed guessing via resources such as vendor documentation, key phrases on public websites, common passwords, and password dumps from public sources.   

* Tools that can be used for this task.  
[Spray365](https://github.com/MarkoH17/Spray365)  
[GoMapEnum](https://github.com/nodauf/GoMapEnum)  

#### TASK: 16.5 – PENETRATION TEST EXTERNAL UNDECLARED HOSTS/NETWORKS  
This task simulates a threat actor’s attempt to gather information about the victim's networks as part of their pre-attack, targeting phase [MITRE ATT&CK ID: T1590](https://attack.mitre.org/techniques/T1590/).  To validate the entity’s knowledge and documentation of allocation assets/networks, a comparison of network exposures in the pre-attack phase is compared to the entity Data Call provided prior to assessment start date.  

* Tools that can be used for this task.  
[Amass](https://github.com/OWASP/Amass)  
[DNSRecon](https://github.com/darkoperator/dnsrecon)  

#### TASK: 16.6 - PENETRATION TEST EXTERNAL HIGH-RISK SERVICE EXPOSURE DETECTION  
This task assesses the entity's exposure of insecure services to the internet [MITRE ATT&CK ID: T1557](https://attack.mitre.org/techniques/T1557/).  Using results from various service analysis techniques of in-scope and undeclared assets.  

Periodically run an all ports NMAP scan  
```
nmap -vv -O -sV -sC -sT -Pn -p 0-65535 --script http-methods --script-args http.useragent="Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36" --open --min-hostgroup 256 --min-parallelism 32 --stylesheet=https://svn.nmap.org/nmap/docs/nmap.xsl -oA entity.name_external_allports -iL /path/to/subnetfile.txt --excludefile /path/to/exclusionfile.txt
```  

#### TASK: 16.7 – PENETRATION TEST EXTERNAL HOST MANAGEMENT SERVICE DETECTION  
This task identifies poorly secured host management services and web application administrative interfaces exposed to the internet [MITRE ATT&CK ID: T1219](https://attack.mitre.org/techniques/T1219/).  

Periodically run an all ports NMAP scan, see TASK 16.6 for NMAP command  

#### TASK: 16.8 – PENETRATION TEST EXTERNAL WEB APPLICATION MISCONFIGURATIONS AND EXPOSURES  
This task identifies and probes selected in-scope and undeclared external websites and web applications to determine potential attack opportunities [MITRE ATT&CK ID: T1190](https://attack.mitre.org/techniques/T1219/).  Research and analysis are conducted to identify exploits and misconfigurations, achieve unauthorized access, detect non-public data exposure, and/or obtain unauthorized remote host access.  

* Tools that can be used for this task.  
[Eyewitness](https://github.com/FortyNorthSecurity/EyeWitness)  
[Burpsuite](https://portswigger.net/burp)  
[ZAP Proxy](https://www.zaproxy.org/)  

#### TASK: 16.9 – PENETRATION TEST EXTERNAL EXECUTION OF MALICIOUS CODE ON CONTROLLED HOST  
The successful exploitation of hosts or services operated, controlled, or provided via 3rd party to the entity.  Exploitation of hosts must occur via the introduction of malicious code execution [MITRE ATT&CK ID: T1204.002](https://attack.mitre.org/techniques/T1204/002/) or host misconfiguration [MITRE ATT&CK ID: T1574](https://attack.mitre.org/techniques/T1574/).  

* Tools that can be used for this task.  
[Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)  
[Mitre Caldera](https://github.com/mitre/caldera)  
[PowerShell Empire](https://github.com/BC-SECURITY/Empire)  
[Sliver](https://github.com/BishopFox/sliver)  

### INTERNAL TASKS  
--------------------  

#### TASK: 17.1 – PENETRATION TEST INTERNAL PASSWORD GUESSING, SPRAYING, AND DEFAULT CREDENTIAL DETECTION  
This task addresses two unique methods of obtaining passwords – password guessing  and password spraying. Password spraying is the process of using informed knowledge such as acquired usernames in combination with common password dictionaries or common entity terminology to guess a username/password combination using brute force techniques [MITRE ATT&CK ID T1110](https://attack.mitre.org/techniques/T1110/).  Default credential testing, when password guessing, utilizes well-known, often public information from application/hardware manufactures installation manuals to inform password guessing attempts on the targeted application/host [MITRE ATT&CK ID T1078](https://attack.mitre.org/techniques/T1078/).  

* Tools that can be used for this task.  
[Spray](https://github.com/Greenwolf/Spray)  
[DomainPasswordSpray](https://github.com/dafthack/DomainPasswordSpray)  

#### TASK: 17.2 – PENETRATION TEST INTERNAL CREDENTIAL HASH CAPTURE AND CRACKING  
This task will assess the entity’s risk exposure to Man-in-the-Middle authenticator hash capture [MITRE ATT&CK ID: T1040](https://attack.mitre.org/techniques/T1040/), hash harvesting from exploited hosts [MITRE ATT&CK ID: T1003](https://attack.mitre.org/techniques/T1003/), and extraction of authenticator hashes from network directory services [MITRE ATT&CK ID: T1558.003](https://attack.mitre.org/techniques/T1558/003/). Captured hashes will be subjected to offline cracking attempts using dictionary and brute force attack methods for a period not to exceed the assessment period to assess cracking resistance [MITRE ATT&CK ID: T1110](https://attack.mitre.org/techniques/T1110/).  

* Tools that can be used to capture hashes.  
[Responder](https://github.com/lgandx/Responder)  
[Inveigh](https://github.com/Kevin-Robertson/Inveigh)  

* Tools that can be used to crack hashes.  
[John the Ripper](https://github.com/openwall/john)  
[Hashcat](https://github.com/hashcat/hashcat)  

Password lists  

* Tools that can be used for this task.  
[Password Lists](https://github.com/danielmiessler/SecLists) 

#### TASK: 17.3 – PENETRATION TEST INTERNAL USE OF INSECURE HOST MANAGEMENT SERVICES  
This task attempts to identify any management service/interface that allows unencrypted access, weak encryption services, utilizes well-known community strings, or can be exploited using remote code execution methods places the entity at enhanced risk [MITRE ATT&CK ID: T1219](https://attack.mitre.org/techniques/T1219/).  

Periodically run an all ports NMAP scan  
```
nmap -vv -O -sV -sC -sT -p 0-65535 --script http-methods --script-args http.useragent="Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36" --open --min-hostgroup 256 --min-parallelism 32 --stylesheet=https://svn.nmap.org/nmap/docs/nmap.xsl -oA entity.name_internal_allports -iL /path/to/subnetfile.txt --excludefile /path/to/exclusionfile.txt
```  

#### TASK: 17.4 – PENETRATION TEST INTERNAL WEB SITE/APPLICATION RISKS  
This task identifies and probes selected in-scope and undeclared, internal websites and web applications to determine potential attack opportunities [MITRE ATT&CK ID: T1190](https://attack.mitre.org/techniques/T1219/).  Research of web risks and analysis are conducted to identify exploits and misconfigurations, achieve unauthorized access, detect non-public data exposure, or obtain unauthorized remote host access.  

* Tools that can be used for this task.  
[Eyewitness](https://github.com/FortyNorthSecurity/EyeWitness)  
[Burpsuite](https://portswigger.net/burp)  
[ZAP Proxy](https://www.zaproxy.org/)   

#### TASK: 17.5 – PENETRATION TEST INTERNAL WIRELESS NETWORK BREACH RESISTANCE  
This task assesses the entity’s protection of their wireless access at the network perimeter.  The successful breach of a wireless network requires the capture of the 4-way handshake between any client and access point.  This data provides a hash value of the credentials required for authentication.  Once captured, a series of dictionary and brute force attacks on the hash can be performed to attempt to crack the password.  

* Tools that can be used for this task.  
[Airgeddon](https://github.com/v1s1t0r1sh3r3/airgeddon)  
[Wifi Pineapple](https://shop.hak5.org/products/wifi-pineapple)  

#### TASK: 17.6 – PENETRATION TEST INTERNAL EXECUTION OF MALICIOUS CODE ON CONTROLLED HOST  
The successful exploitation of hosts or services operated, controlled, or provided via 3rd party to the entity.  Exploitation of hosts must occur via the introduction of malicious code execution [MITRE ATT&CK ID: T1204.002](https://attack.mitre.org/techniques/T1204/002/) or host misconfiguration [MITRE ATT&CK ID: T1574](https://attack.mitre.org/techniques/T1574/).  

* Tools that can be used for this task.  
[Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)  
[Mitre Caldera](https://github.com/mitre/caldera)  
[PowerShell Empire](https://github.com/BC-SECURITY/Empire)  
[Sliver](https://github.com/BishopFox/sliver)  

### Third Party Security Assessment Docs  
[SalesForce Security Assessment](https://help.salesforce.com/s/articleView?id=000394469&type=1)  
[SalesForce Security Assessment Agreement](https://help.salesforce.com/s/articleView?id=000392845&type=1)  
[Google Cloud Platform Acceptable Use Policy](https://cloud.google.com/terms/aup)  
[Google Cloud Platform Terms of Service](https://cloud.google.com/terms/)  
[AWS Customer Support Policy for Penetration Testing](https://aws.amazon.com/security/penetration-testing/)  
[Wordpress.com Security Assessment](https://wordpress.com/support/security/#security-testing)  
[Wordpress.com HackerOne Bug Bounty Program](https://hackerone.com/automattic?type=team)  
