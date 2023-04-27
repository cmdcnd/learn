The Domain Controller Security Policy is pretty straight forward and should not require any specific changes for your organization.  The one thing you might have to watch out for are devices that query AD for authentication.  The GPO forces signed LDAP which requires certificates for the the DCs.  It also forces NTLM V2 which some older devices are unable to use.  The best option is to upgrade the devices so they can support NTLM V2.  

### References  
[Group Policy Files](https://github.com/cmdcnd/learn/tree/main/docs/Microsoft/GroupPolicy/domaincontroller/Computer-Security) 