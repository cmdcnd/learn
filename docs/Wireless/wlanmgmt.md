## WLAN-ND-000100  
### Group Title:
The password configured on the WLAN access point for key generation and client access must be set to a 15-character or longer complex password as required by USCYBERCOM CTO 07-15 Rev1.  

### Rule Title:
The password configured on the WLAN access point for key generation and client access must be set to a 15-character or longer complex password as required by USCYBERCOM CTO 07-15 Rev1.  

### Fix Text:
Configure the key generation password on the WLAN Access Point to a 15-character or longer complex password on access points that do not use AAA servers for authentication.  

### Discussion:
If the organization does not use a strong passcode for client access, an adversary is significantly more likely to be able to obtain it. Once this occurs, the adversary may be able to obtain full network access, obtain DoD sensitive information, and attack other DoD information systems.  

### CCIs:
CCI-000205
The information system enforces minimum password length.
NIST SP 800-53::IA-5 (1) (a)
NIST SP 800-53 Revision 4::IA-5 (1) (a)
NIST SP 800-53A::IA-5 (1).1 (i)  

### Check Content:
This check only applies to access points that do not use an AAA (RADIUS) server for authentication services. In most cases, this means the access point is configured for WPA2/WPA3 (Personal), which relies on password authentication, and not WPA2/WPA3 (Enterprise), which uses a AAA server to authenticate each user based on that user's authentication credentials. 

Verify the client authentication password has been set on the access point with the following settings:
- 15 characters or more
- The authentication password selected use at least two of each of the following: uppercase letter, lowercase letter, number, and special character. 

The procedure for verifying these settings varies between AP models. Have the SA show the settings in the AP management console.

If the WLAN client password is not configured for at least a 15-character length and a complexity with at least two each of uppercase letters, lowercase letters, numbers, and special characters, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000200  
### Group Title:
The network device must enforce a minimum 15-character password length.  

### Rule Title:
The network device must enforce a minimum 15-character password length.  

### Fix Text:
Configure the network device so it will require a password to gain administrative access to the device. Configure the password length to at least 15 characters.  

### Discussion:
Password complexity, or strength, is a measure of the effectiveness of a password in resisting attempts at guessing and brute-force attacks. Password length is one factor of several that helps to determine strength and how long it takes to crack a password.

The shorter the password, the lower the number of possible combinations that need to be tested before the password is compromised. Use of more characters in a password helps to exponentially increase the time and/or resources required to compromise the password.  

### CCIs:
CCI-000205
The information system enforces minimum password length.
NIST SP 800-53::IA-5 (1) (a)
NIST SP 800-53 Revision 4::IA-5 (1) (a)
NIST SP 800-53A::IA-5 (1).1 (i)  

### Check Content:
Review the network device configuration to determine if the network device is configured with a password of at least 15 characters.

If the network device password is not at least 15 characters in length, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000300   
### Group Title:
The network device must not have any default manufacturer passwords when deployed.  

### Rule Title:
The network device must not have any default manufacturer passwords when deployed.  

### Fix Text:
Remove any vendor default passwords from the network device configuration.  

### Discussion:
Network devices not protected with strong password schemes provide the opportunity for anyone to crack the password and gain access to the device, which can result in loss of availability, confidentiality, or integrity of network traffic. 

Many default vendor passwords are well known or easily guessed; therefore, not removing them prior to deploying the network device into production provides an opportunity for a malicious user to gain unauthorized access to the device.  

### CCIs:
CCI-002041
The information system allows the use of a temporary password for system logons with an immediate change to a permanent password.
NIST SP 800-53 Revision 4::IA-5 (1) (f)  

### Check Content:
Review the network device configuration to determine if the vendor default password is active.

If any vendor default passwords are used on the device, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000400   
### Group Title:
The network device must display the Standard Mandatory DoD Notice and Consent Banner before granting access to the device.  

### Rule Title:
The network device must display the Standard Mandatory DoD Notice and Consent Banner before granting access to the device.  

### Fix Text:
Configure all management interfaces to the network device to display the DoD-mandated warning banner verbiage at logon regardless of the means of connection or communication. The required banner verbiage that must be displayed verbatim as follows:

Option A

You are accessing a U.S. Government (USG) Information System (IS) that is provided for USG-authorized use only.

By using this IS (which includes any device attached to this IS), you consent to the following conditions:

-The USG routinely intercepts and monitors communications on this IS for purposes including, but not limited to, penetration testing, COMSEC monitoring, network operations and defense, personnel misconduct (PM), law enforcement (LE), and counterintelligence (CI) investigations.

-At any time, the USG may inspect and seize data stored on this IS.

-Communications using, or data stored on, this IS are not private, are subject to routine monitoring, interception, and search, and may be disclosed or used for any USG-authorized purpose.

-This IS includes security measures (e.g., authentication and access controls) to protect USG interests--not for your personal benefit or privacy.

-Notwithstanding the above, using this IS does not constitute consent to PM, LE or CI investigative searching or monitoring of the content of privileged communications, or work product, related to personal representation or services by attorneys, psychotherapists, or clergy, and their assistants. Such communications and work product are private and confidential. See User Agreement for details.

Option B

If the system is incapable of displaying the required banner verbiage due to its size, a smaller banner must be used. The mandatory verbiage follows: "I've read & consent to terms in IS user agreem't."  

### Discussion:
All network devices must present a DoD-approved warning banner prior to a system administrator logging on. The banner should warn any unauthorized user not to proceed. It also should provide clear and unequivocal notice to both authorized and unauthorized personnel that access to the device is subject to monitoring to detect unauthorized usage. Failure to display the required logon warning banner prior to logon attempts limits DoD's ability to prosecute unauthorized access and also presents the potential for criminal and civil liability for systems administrators and information systems managers. In addition, DISA's ability to monitor the device's usage is limited unless a proper warning banner is displayed.

DoD CIO has issued new, mandatory policy standardizing the wording of "notice and consent" banners and matching user agreements for all Secret and below DoD information systems, including stand-alone systems by releasing DoD CIO Memo, "Policy on Use of Department of Defense (DoD) Information Systems Standard Consent Banner and User Agreement", dated 9 May 2008. The banner is mandatory and deviations are not permitted except as authorized in writing by the Deputy Assistant Secretary of Defense for Information and Identity Assurance. Implementation of this banner verbiage is further directed to all DoD components for all DoD assets via USCYBERCOM CTO 08-008A.  

### CCIs:
CCI-000048
Display an organization-defined system use notification message or banner to users before granting access to the system that provides privacy and security notices consistent with applicable federal laws, Executive Orders, directives, policies, regulations, standards, and guidelines.
NIST SP 800-53::AC-8 a
NIST SP 800-53 Revision 4::AC-8 a
NIST SP 800-53 Revision 5::AC-8 a
NIST SP 800-53A::AC-8.1 (ii)  

### Check Content:
Review the device configuration or request that the administrator log on to the device and observe the terminal. 

Verify either Option A or Option B (for systems with character limitations) of the Standard Mandatory DoD Notice and Consent Banner is displayed at logon. The required banner verbiage follows and must be displayed verbatim:

Option A

You are accessing a U.S. Government (USG) Information System (IS) that is provided for USG-authorized use only. 

By using this IS (which includes any device attached to this IS), you consent to the following conditions:

-The USG routinely intercepts and monitors communications on this IS for purposes including, but not limited to, penetration testing, COMSEC monitoring, network operations and defense, personnel misconduct (PM), law enforcement (LE), and counterintelligence (CI) investigations.

-At any time, the USG may inspect and seize data stored on this IS.

-Communications using, or data stored on, this IS are not private, are subject to routine monitoring, interception, and search, and may be disclosed or used for any USG-authorized purpose.

-This IS includes security measures (e.g., authentication and access controls) to protect USG interests--not for your personal benefit or privacy.

-Notwithstanding the above, using this IS does not constitute consent to PM, LE or CI investigative searching or monitoring of the content of privileged communications, or work product, related to personal representation or services by attorneys, psychotherapists, or clergy, and their assistants. Such communications and work product are private and confidential. See User Agreement for details.

Option B

If the system is incapable of displaying the required banner verbiage due to its size, a smaller banner must be used. The mandatory verbiage follows: "I've read & consent to terms in IS user agreem't."

If the device configuration does not have a logon banner as stated above, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000500    
### Group Title:
The network device must terminate all network connections associated with a device management session at the end of the session, or the session must be terminated after 10 minutes of inactivity except to fulfill documented and validated mission requirements.  

### Rule Title:
The network device must terminate all network connections associated with a device management session at the end of the session, or the session must be terminated after 10 minutes of inactivity except to fulfill documented and validated mission requirements.  

### Fix Text:
Configure the network devices to ensure the timeout for unattended administrative access connections is no longer than 10 minutes.  

### Discussion:
Terminating an idle session within a short time period reduces the window of opportunity for unauthorized personnel to take control of a management session enabled on the console or console port that has been left unattended. Quickly terminating an idle session will also free up resources committed by the managed network element. 

Terminating network connections associated with communications sessions includes, for example, deallocating associated TCP/IP address/port pairs at the operating system level or deallocating networking assignments at the application level if multiple application sessions are using a single, operating system-level network connection. This does not mean that the device terminates all sessions or network access; it only ends the inactive session and releases the resources associated with that session.  

### CCIs:
CCI-001133
Terminate the network connection associated with a communications session at the end of the session or after an organization-defined time period of inactivity.
NIST SP 800-53::SC-10
NIST SP 800-53 Revision 4::SC-10
NIST SP 800-53 Revision 5::SC-10
NIST SP 800-53A::SC-10.1 (ii)  

### Check Content:
Review the management connection for administrative access and verify the network device is configured to time-out the connection at 10 minutes or less of inactivity.

If the device does not terminate inactive management connections at 10 minutes or less, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000600   
### Group Title:
The network device must be configured to authenticate each administrator prior to authorizing privileges based on assignment of group or role.  

### Rule Title:
The network device must be configured to authenticate each administrator prior to authorizing privileges based on assignment of group or role.  

### Fix Text:
Configure the network device to authenticate users before assigning privileges to each individual user account based on the role or group the account is assigned to.  

### Discussion:
To ensure individual accountability and prevent unauthorized access, administrators must be individually identified and authenticated.

Individual accountability mandates that each administrator is uniquely identified. A group authenticator is a shared account or some other form of authentication that allows multiple unique individuals to access the network device using a single account. 

If a device allows or provides for group authenticators, it must individually authenticate administrators prior to implementing group authenticator functionality. 

Some devices may not have the need to provide a group authenticator; this is considered a matter of device design. Where the device design includes the use of a group authenticator, this requirement will apply. This requirement applies to accounts created and managed on or by the network device.  

### CCIs:
CCI-000770
The organization requires individuals to be authenticated with an individual authenticator when a group authenticator is employed.
NIST SP 800-53::IA-2 (5) (b)
NIST SP 800-53 Revision 4::IA-2 (5)
NIST SP 800-53A::IA-2 (5).2 (ii)  

### Check Content:
Review the network device configuration and validate that users are authenticated before they are assigned privileges based on the role or group the account is assigned to.

If a user can gain access to network device privileges before they are authenticated, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000700  
### Group Title:
The network device must enforce the assigned privilege level for each administrator and authorizations for access to all commands relative to the privilege level in accordance with applicable policy for the device.  

### Rule Title:
The network device must enforce the assigned privilege level for each administrator and authorizations for access to all commands relative to the privilege level in accordance with applicable policy for the device.  

### Fix Text:
Configure authorized accounts with the least privilege rule. Each user will have access to only the privileges they require to perform their assigned duties.  

### Discussion:
To mitigate the risk of unauthorized access to sensitive information by entities that have been issued certificates by DoD-approved PKIs, all DoD systems must be properly configured to incorporate access control methods that do not rely solely on the possession of a certificate for access. 

Successful authentication must not automatically give an entity access to an asset or security boundary. Authorization procedures and controls must be implemented to ensure each authenticated entity also has a validated and current authorization. Authorization is the process of determining whether an entity, once authenticated, is permitted to access a specific asset. Network devices use access control policies and enforcement mechanisms to implement this requirement. 

Access control policies include identity-based policies, role-based policies, and attribute-based policies. Access enforcement mechanisms include access control lists, access control matrices, and cryptography. These policies and mechanisms must be employed by the network device to control access between administrators (or processes acting on behalf of administrators) and objects (e.g., device commands, files, records, processes) in the network device.  

### CCIs:
CCI-000213
Enforce approved authorizations for logical access to information and system resources in accordance with applicable access control policies.
NIST SP 800-53::AC-3
NIST SP 800-53 Revision 4::AC-3
NIST SP 800-53 Revision 5::AC-3
NIST SP 800-53A::AC-3.1  

### Check Content:
Review the accounts authorized for access to the network device. Determine if the accounts are assigned the lowest privilege level necessary to perform assigned duties. User accounts must be set to a specific privilege level, which can be mapped to specific commands or a group of commands. Authorized accounts should have the least privilege level unless deemed necessary for assigned duties.

If authorized accounts are assigned to greater privileges than necessary, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000800  
### Group Title:
The network device must be configured to implement cryptographic mechanisms using a FIPS 140-2 approved algorithm to protect the confidentiality of remote maintenance sessions.  

### Rule Title:
The network device must be configured to implement cryptographic mechanisms using a FIPS 140-2 approved algorithm to protect the confidentiality of remote maintenance sessions.  

### Fix Text:
Configure the network device to use secure protocols with FIPS 140-2 validated cryptographic modules.  

### Discussion:
This requires the use of secure protocols instead of their unsecured counterparts, such as SSH instead of telnet, SCP instead of FTP, and HTTPS instead of HTTP. If unsecured protocols (lacking cryptographic mechanisms) are used for sessions, the contents of those sessions will be susceptible to eavesdropping, potentially putting sensitive data (including administrator passwords) at risk of compromise and potentially allowing hijacking of maintenance sessions.  

### CCIs:
CCI-003123
Implement organization-defined cryptographic mechanisms to protect the confidentiality of nonlocal maintenance and diagnostic communications.
NIST SP 800-53 Revision 4::MA-4 (6)
NIST SP 800-53 Revision 5::MA-4 (6)  

### Check Content:
Review the network device configuration to verify only secure protocols using FIPS 140-2 validated cryptographic modules are used for any administrative access. Some of the secure protocols used for administrative and management access are listed below. This list is not all inclusive and represents a sample selection of secure protocols. 

- SSHv2
- SCP
- HTTPS using TLS

If management connections are established using protocols without FIPS 140-2 validated cryptographic modules, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-000900  
### Group Title:
The network device must generate audit records when successful/unsuccessful logon attempts occur.  

### Rule Title:
The network device must generate audit records when successful/unsuccessful logon attempts occur.  

### Fix Text:
Configure the device to log all access attempts to the device to establish a management connection for administrative access.  

### Discussion:
Without generating audit records that are specific to the security and mission needs of the organization, it would be difficult to establish, correlate, and investigate the events relating to an incident or identify those responsible for one.

Audit records can be generated from various components within the network device (e.g., module or policy filter).  

### CCIs:
CCI-000172
Generate audit records for the event types defined in AU-2 c that include the audit record content defined in AU-3.
NIST SP 800-53::AU-12 c
NIST SP 800-53 Revision 4::AU-12 c
NIST SP 800-53 Revision 5::AU-12 c
NIST SP 800-53A::AU-12.1 (iv)  

### Check Content:
Review the configuration to verify all attempts to access the device via management connection are logged.

If management connection attempts are not logged, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001000  
### Group Title:
The network device must be running an operating system release that is currently supported by the vendor.  

### Rule Title:
The network device must be running an operating system release that is currently supported by the vendor.  

### Fix Text:
Update the operating system to a supported version that addresses all related IAVMs.  

### Discussion:
Network devices running an unsupported operating system lack current security fixes required to mitigate the risks associated with recent vulnerabilities.  

### CCIs:
CCI-000366
Implement the security configuration settings.
NIST SP 800-53::CM-6 b
NIST SP 800-53 Revision 4::CM-6 b
NIST SP 800-53 Revision 5::CM-6 b
NIST SP 800-53A::CM-6.1 (iv)  

### Check Content:
Have the administrator display the operating system version in operation. The operating system must be current, with related IAVMs addressed.

If the device is using an OS that does not meet all IAVMs or is not currently supported by the vendor, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001100  
### Group Title:
The network device must be configured to use an authentication server to authenticate users prior to granting administrative access.  

### Rule Title:
The network device must be configured to use an authentication server to authenticate users prior to granting administrative access.  

### Fix Text:
Configure authentication for all management connections using an authentication server.  

### Discussion:
Centralized management of authentication settings increases the security of remote and nonlocal access methods. This is particularly important protection against the insider threat. With robust centralized management, audit records for administrator account access to the organization's network devices can be more readily analyzed for trends and anomalies. The alternative method of defining administrator accounts on each device exposes the device configuration to remote access authentication attacks and system administrators with multiple authenticators for each network device.  

### CCIs:
CCI-000366
Implement the security configuration settings.
NIST SP 800-53::CM-6 b
NIST SP 800-53 Revision 4::CM-6 b
NIST SP 800-53 Revision 5::CM-6 b
NIST SP 800-53A::CM-6.1 (iv)
CCI-000370
Manage configuration settings for organization-defined system components using organization-defined automated mechanisms.
NIST SP 800-53::CM-6 (1)
NIST SP 800-53 Revision 4::CM-6 (1)
NIST SP 800-53 Revision 5::CM-6 (1)
NIST SP 800-53A::CM-6 (1).1  

### Check Content:
Review the network device configuration to verify all management connections use an authentication server for administrative access.

If the network device is not configured to use an authentication server for management access, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001200    
### Group Title:
The network device must be configured to authenticate SNMP messages using a FIPS-validated Keyed-Hash Message Authentication Code (HMAC).  

### Rule Title:
The network device must be configured to authenticate SNMP messages using a FIPS-validated Keyed-Hash Message Authentication Code (HMAC).  

### Fix Text:
If SNMP is enabled, configure the network device to use SNMP Version 3 Security Model with FIPS 140-2 validated cryptography (i.e., SHA authentication and AES encryption).  

### Discussion:
Without authenticating devices, unidentified or unknown devices may be introduced, thereby facilitating malicious activity. Bidirectional authentication provides stronger safeguards to validate the identity of other devices for connections that are of greater risk.

A local connection is any connection with a device communicating without the use of a network. A network connection is any connection with a device that communicates through a network (e.g., local area or wide area network, internet). A remote connection is any connection with a device communicating through an external network (e.g., the internet).

Because of the challenges of applying this requirement on a large scale, organizations are encouraged to only apply the requirement to those limited number (and types) of devices that truly need to support this capability.  

### CCIs:
CCI-001967
Authenticate organization-defined devices and/or types of devices before establishing a local, remote, and/or network connection using bidirectional authentication that is cryptographically based.
NIST SP 800-53 Revision 4::IA-3 (1)
NIST SP 800-53 Revision 5::IA-3 (1)  

### Check Content:
Review the device configuration to verify it is configured to use SNMPv3 with both SHA authentication and privacy using AES encryption.

If the device is not configured to use SNMP, this is not a finding.

If the device is configured to use to anything other than SNMPv3 with at least SHA-1 and AES, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001300    
### Group Title:
The network device must be configured with only one local account to be used as the account of last resort in the event the authentication server is unavailable.  

### Rule Title:
The network device must be configured with only one local account to be used as the account of last resort in the event the authentication server is unavailable.  

### Fix Text:
Configure the device to allow only one local account of last resort for emergency access and store the credentials in a secure manner.  

### Discussion:
Authentication for administrative (privileged level) access to the device is required at all times. An account can be created on the device's local database for use when the authentication server is down or connectivity between the device and the authentication server is not operable. This account is referred to as the account of last resort since it is intended to be used as a last resort and when immediate administrative access is absolutely necessary.

The account of last resort logon credentials must be stored in a sealed envelope and kept in a safe. The safe must be periodically audited to verify the envelope remains sealed. The signature of the auditor and the date of the audit should be added to the envelope as a record. Administrators should secure the credentials and disable the root account (if possible) when not needed for system administration functions.  

### CCIs:
CCI-001358
Establish privileged user accounts in accordance with a role-based access scheme; or an attribute-based access scheme.
NIST SP 800-53::AC-2 (7) (a)
NIST SP 800-53 Revision 4::AC-2 (7) (a)
NIST SP 800-53 Revision 5::AC-2 (7) (a)
NIST SP 800-53A::AC-2 (7).1 (i)
CCI-002111
The organization identifies and selects the organization-defined information system account types of information system accounts which support organizational missions/business functions.
NIST SP 800-53 Revision 4::AC-2 a  

### Check Content:
Review the network device configuration to determine if an authentication server is defined for gaining administrative access. If so, there must be only one account of last resort configured locally for an emergency.

Verify the username and password for the local account of last resort is contained in a sealed envelope kept in a safe.

If an authentication server is used and more than one local account exists, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001400    
### Group Title:
The network device must be configured to enforce the limit of three consecutive invalid logon attempts, after which time it must block any login attempt for 15 minutes.  

### Rule Title:
The network device must be configured to enforce the limit of three consecutive invalid logon attempts, after which time it must block any login attempt for 15 minutes.  

### Fix Text:
Configure the network device to require a maximum number of unsuccessful SSH logon attempts at "3", after which time it must block any login attempt for 15 minutes.  

### Discussion:
By limiting the number of failed login attempts, the risk of unauthorized system access via user password guessing, otherwise known as brute forcing, is reduced.  

### CCIs:
CCI-000044
Enforce the organization-defined limit of consecutive invalid logon attempts by a user during the organization-defined time period.
NIST SP 800-53::AC-7 a
NIST SP 800-53 Revision 4::AC-7 a
NIST SP 800-53 Revision 5::AC-7 a
NIST SP 800-53A::AC-7.1 (ii)  

### Check Content:
Review the configuration and verify the number of unsuccessful SSH logon attempts is set at "3", after which time it must block any login attempt for 15 minutes.

If the device is not configured to reset unsuccessful SSH logon attempts at "3" and then block any login attempt for 15 minutes, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001500  
### Group Title:
The network device must be configured to prohibit the use of all unnecessary and/or nonsecure functions, ports, protocols, and/or services.  

### Rule Title:
The network device must be configured to prohibit the use of all unnecessary and/or nonsecure functions, ports, protocols, and/or services.  

### Fix Text:
Configure the network device to prohibit the use of all unnecessary and/or nonsecure functions, ports, protocols, and/or services.  

### Discussion:
To prevent unauthorized connection of devices, unauthorized transfer of information, or unauthorized tunneling (i.e., embedding of data types within data types), organizations must disable unused or unnecessary physical and logical ports/protocols on information systems.

Network devices are capable of providing a wide variety of functions and services. Some of the functions and services provided by default may not be necessary to support essential organizational operations. Additionally, it is sometimes convenient to provide multiple services from a single component (e.g., email and web services); however, doing so increases risk over limiting the services provided by any one component. 

To support the requirements and principles of least functionality, the network device must support the organizational requirements, providing only essential capabilities and limiting the use of ports, protocols, and/or services to only those required, authorized, and approved. Some network devices have capabilities enabled by default; if these capabilities are not necessary, they must be disabled. If a particular capability is used, it must be documented and approved.  

### CCIs:
CCI-000382
Configure the system to prohibit or restrict the use of organization-defined prohibited or restricted functions, system ports, protocols, software, and/or services.
NIST SP 800-53::CM-7
NIST SP 800-53 Revision 4::CM-7 b
NIST SP 800-53 Revision 5::CM-7 b
NIST SP 800-53A::CM-7.1 (iii)  

### Check Content:
Review the configuration of the network device. Verify all unnecessary and/or nonsecure functions, ports, protocols, and/or services are disabled.

If any unnecessary and/or nonsecure functions, ports, protocols, and/or services are not disabled, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001600  
### Group Title:
The network device must authenticate Network Time Protocol (NTP) sources using authentication that is cryptographically based.  

### Rule Title:
The network device must authenticate Network Time Protocol (NTP) sources using authentication that is cryptographically based.  

### Fix Text:
Configure the device to authenticate all received NTP messages using a FIPS-approved message authentication code algorithm.  

### Discussion:
If Network Time Protocol is not authenticated, an attacker can introduce a rogue NTP server. This rogue server can then be used to send incorrect time information to network devices, which will make log timestamps inaccurate and affect scheduled actions. NTP authentication is used to prevent this tampering by authenticating the time source.  

### CCIs:
CCI-001967
Authenticate organization-defined devices and/or types of devices before establishing a local, remote, and/or network connection using bidirectional authentication that is cryptographically based.
NIST SP 800-53 Revision 4::IA-3 (1)
NIST SP 800-53 Revision 5::IA-3 (1)  

### Check Content:
Review the network device configuration to determine if the network device authenticates NTP endpoints before establishing a local, remote, or network connection using authentication that is cryptographically based.

If the network device does not authenticate Network Time Protocol sources using authentication that is cryptographically based, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001700   
### Group Title:
The network device must implement replay-resistant authentication mechanisms for network access to privileged accounts.  

### Rule Title:
The network device must implement replay-resistant authentication mechanisms for network access to privileged accounts.  

### Fix Text:
Configure the network device to use SSH Version 2.  

### Discussion:
A replay attack may enable an unauthorized user to gain access to the application. Authentication sessions between the authenticator and the application validating the user credentials must not be vulnerable to a replay attack.

An authentication process resists replay attacks if it is impractical to achieve a successful authentication by recording and replaying a previous authentication message. 

Techniques used to address this include protocols using nonces (e.g., numbers generated for a specific one-time use) or challenges (e.g., TLS, WS_Security). Additional techniques include time-synchronous or challenge-response one-time authenticators.  

### CCIs:
CCI-001941
Implement replay-resistant authentication mechanisms for access to privileged accounts and/or non-privileged accounts.
NIST SP 800-53 Revision 4::IA-2 (8)
NIST SP 800-53 Revision 5::IA-2 (8)  

### Check Content:
Review the configuration and verify SSH Version 1 is not being used for administrative access.

If the device is using an SSHv1 session, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001800   
### Group Title:
The network device must be configured with both an ingress and egress ACL.  

### Rule Title:
The network device must be configured with both an ingress and egress ACL.  

### Fix Text:
If the management interface is a routed interface, configure it with both an ingress and egress ACL. The ingress ACL should block any transit traffic, while the egress ACL should block any traffic that was not originated by the managed network device.  

### Discussion:
Changes to the hardware or software components of the network device can have significant effects on the overall security of the network. Therefore, only qualified and authorized individuals should be allowed administrative access to the network device for implementing any changes or upgrades. This requirement applies to updates of the application files, configuration, ACLs, and policy filters.  

### CCIs:
CCI-000345
Enforce logical access restrictions associated with changes to the system.
NIST SP 800-53::CM-5
NIST SP 800-53 Revision 4::CM-5
NIST SP 800-53 Revision 5::CM-5
NIST SP 800-53A::CM-5.1
CCI-000366
Implement the security configuration settings.
NIST SP 800-53::CM-6 b
NIST SP 800-53 Revision 4::CM-6 b
NIST SP 800-53 Revision 5::CM-6 b
NIST SP 800-53A::CM-6.1 (iv)  

### Check Content:
1. Verify the managed interface has an inbound and outbound ACL or filter.

2. Verify the ingress ACL blocks all transit traffic (any traffic not destined to the router itself). In addition, traffic accessing the managed elements should be originated at the NOC.

3. Verify the egress ACL blocks any traffic not originated by the managed element.

If the management interface does not have an ingress and egress filter configured and applied, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

## WLAN-ND-001900  
### Group Title:
The network device must be configured to synchronize internal information system clocks using redundant authoritative time sources.  

### Rule Title:
The network device must be configured to synchronize internal information system clocks using redundant authoritative time sources.  

### Fix Text:
Configure the device to synchronize internal information system clocks using redundant authoritative time sources.  

### Discussion:
The loss of connectivity to a particular authoritative time source will result in the loss of time synchronization (free-run mode) and increasingly inaccurate time stamps on audit events and other functions.

Multiple time sources provide redundancy by including a secondary source. Time synchronization is usually a hierarchy; clients synchronize time to a local source while that source synchronizes its time to a more accurate source. The network device must use an authoritative time server and/or be configured to use redundant authoritative time sources. This requirement is related to the comparison done in CCI-001891.

DoD-approved solutions consist of a combination of a primary and secondary time source using a combination or multiple instances of the following: a time server designated for the appropriate DoD network (NIPRNet/SIPRNet); United States Naval Observatory (USNO) time servers; and/or the Global Positioning System (GPS). The secondary time source must be located in a different geographic region than the primary time source.  

### CCIs:
CCI-000366
Implement the security configuration settings.
NIST SP 800-53::CM-6 b
NIST SP 800-53 Revision 4::CM-6 b
NIST SP 800-53 Revision 5::CM-6 b
NIST SP 800-53A::CM-6.1 (iv)
CCI-001893
The information system identifies a secondary authoritative time source that is located in a different geographic region than the primary authoritative time source.
NIST SP 800-53 Revision 4::AU-8 (2)  

### Check Content:
Review the configuration and verify the network device synchronizes internal information system clocks using redundant authoritative time sources.

If the device is not configured to synchronize internal information system clocks using redundant authoritative time sources, this is a finding.  

### Check Content Ref:
undefined:U_Network_WLAN_AP-IG_Mgmt_STIG_V7R2_Manual-xccdf.xml  

### Weight:
10.0  

### Documentable:
false  

---

