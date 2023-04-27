This policy has the basic user security settings for Java.  The best way to setup Java is make all the configuration settings for java on your local computer, such as Exceptions sites and any changes needed under advanced security, then copy it to a network location.

* Copy the following files from c:\users\%username%\AppData\LocalLow\Sun\Java\Deployment\Security\  
	* exception.sites  
	* trusted.certs  
	* trusted.jssecerts  

* Copy the following files from c:\users\%username%\AppData\LocalLow\Sun\Java\Deployment\  
	* deployment.properties  
* Group Policy Preferences  
	* Adjust the Java registry settings to copy the files from a network location that users have read access to.  

	### References  
[Group Policy Files](https://github.com/cmdcnd/learn/tree/main/docs/Microsoft/GroupPolicy/client/User-Security)  