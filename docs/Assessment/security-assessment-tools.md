### Security Assessment Tools  
[Kali Image](https://www.kali.org/get-kali/#kali-installer-images)  
[Manidant Commando](https://github.com/mandiant/commando-vm)  

#### EXTERNAL TASKS  
--------------------  
##### TASK: 16.1 – PENETRATION TEST EXTERNAL OPEN-SOURCE META DATA IDENTITY COLLECTION  
* [SimplyEmail](https://github.com/SimplySecurity/SimplyEmail)  
* [FOCA](https://github.com/ElevenPaths/FOCA)  

##### TASK: 16.2 – PENETRATION TEST EXTERNAL SPEAR PHISHING ATTEMPT  
* [Attack simulation training M365](https://docs.microsoft.com/en-us/microsoft-365/security/office-365-security/attack-simulation-training?view=o365-worldwide)  

##### TASK: 16.3 – PENETRATION TEST EXTERNAL PASSWORD GUESSING ACTIVITIES  
* [Spray365](https://github.com/MarkoH17/Spray365)  
* [GoMapEnum](https://github.com/nodauf/GoMapEnum)  

##### TASK: 16.5 – PENETRATION TEST EXTERNAL UNDECLARED HOSTS/NETWORKS  
* [Amass](https://github.com/OWASP/Amass)  
* [DNSRecon](https://github.com/darkoperator/dnsrecon)  

##### TASK: 16.6 - PENETRATION TEST EXTERNAL HIGH-RISK SERVICE EXPOSURE DETECTION  
Periodically run an all ports NMAP scan  
```
nmap -vv -O -sV -sC -sT -Pn -p 0-65535 --script http-methods --script-args http.useragent="Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36" --open --min-hostgroup 256 --min-parallelism 32 --stylesheet=https://svn.nmap.org/nmap/docs/nmap.xsl -oA entity.name_external_allports -iL /path/to/subnetfile.txt --excludefile /path/to/exclusionfile.txt
```  

##### TASK: 16.7 – PENETRATION TEST EXTERNAL HOST MANAGEMENT SERVICE DETECTION  
Periodically run an all ports NMAP scan, see TASK 16.6 for NMAP command  

##### TASK: 16.8 – PENETRATION TEST EXTERNAL WEB APPLICATION MISCONFIGURATIONS AND EXPOSURES  
* [Eyewitness](https://github.com/FortyNorthSecurity/EyeWitness)  
* [Burpsuite](https://portswigger.net/burp)  
* [ZAP Proxy](https://www.zaproxy.org/)  

##### TASK: 16.9 – PENETRATION TEST EXTERNAL EXECUTION OF MALICIOUS CODE ON CONTROLLED HOST  
* [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)  
* [Mitre Caldera](https://github.com/mitre/caldera)  

#### INTERNAL TASKS  
--------------------  

##### TASK: 17.1 – PENETRATION TEST INTERNAL PASSWORD GUESSING, SPRAYING, AND DEFAULT CREDENTIAL DETECTION  
* [Spray](https://github.com/Greenwolf/Spray)  
* [DomainPasswordSpray](https://github.com/dafthack/DomainPasswordSpray)  

##### TASK: 17.2 – PENETRATION TEST INTERNAL CREDENTIAL HASH CAPTURE AND CRACKING  
Tools to capture hashes  

* [Responder](https://github.com/lgandx/Responder)  
* [Inveigh](https://github.com/Kevin-Robertson/Inveigh)  

Tools to crack hashes  

* [John the Ripper](https://github.com/openwall/john)  
* [Hashcat](https://github.com/hashcat/hashcat)  

Password lists  

* [Password Lists](https://github.com/danielmiessler/SecLists) 

##### TASK: 17.3 – PENETRATION TEST INTERNAL USE OF INSECURE HOST MANAGEMENT SERVICES  
Periodically run an all ports NMAP scan  
```
nmap -vv -O -sV -sC -sT -p 0-65535 --script http-methods --script-args http.useragent="Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.120 Safari/537.36" --open --min-hostgroup 256 --min-parallelism 32 --stylesheet=https://svn.nmap.org/nmap/docs/nmap.xsl -oA entity.name_internal_allports -iL /path/to/subnetfile.txt --excludefile /path/to/exclusionfile.txt
```  

##### TASK: 17.4 – PENETRATION TEST INTERNAL WEB SITE/APPLICATION RISKS  
* [Eyewitness](https://github.com/FortyNorthSecurity/EyeWitness)  
* [Burpsuite](https://portswigger.net/burp)  
* [ZAP Proxy](https://www.zaproxy.org/)   

##### TASK: 17.5 – PENETRATION TEST INTERNAL WIRELESS NETWORK BREACH RESISTANCE  
* [Airgeddon](https://github.com/v1s1t0r1sh3r3/airgeddon)  
* [Wifi Pineapple](https://shop.hak5.org/products/wifi-pineapple)  

##### TASK: 17.6 – PENETRATION TEST INTERNAL EXECUTION OF MALICIOUS CODE ON CONTROLLED HOST  
* [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)  
* [Mitre Caldera](https://github.com/mitre/caldera)  