### Deploy Tenable.io Nessus Agent  
Using the instructions from [Intune Deploy App](#intune-deploy-app) deploy Nessus agent.  

* Deploy MSI via `Windows MSI line-of-business app`  
* App install context: Device  
* Ignore app version: Yes  
* Command-line arguments: /qn NESSUS_SERVER=cloud.tenable.com:443 NESSUS_KEY=PUT_YOUR_LINKING_KEY_HERE  


## References  
### [Intune Deploy App](https://learn.microsoft.com/en-us/mem/intune/apps/lob-apps-windows)  