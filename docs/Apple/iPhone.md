## Step-by-Step Guide to Secure an Apple iPhone  
### 1. Update iOS Regularly  
- **Why**: Updates fix security vulnerabilities and enhance performance.  
- **How**:  
  1. Go to **Settings > General > Software Update**.  
  2. Enable **Automatic Updates** to install updates automatically.  

### 2. Enable Strong Passcodes and Biometrics  
- **Why**: Prevent unauthorized access.  
- **How**:  
  1. Go to **Settings > Face ID & Passcode (or Touch ID & Passcode)**.  
  2. Set a 6-digit or alphanumeric passcode.  
  3. Enable Face ID or Touch ID for secure access.  

### 3. Use Two-Factor Authentication (2FA) for Apple ID  
- **Why**: Adds a layer of protection to your Apple ID.  
- **How**:  
  1. Go to **Settings > [Your Name] > Password & Security**.  
  2. Enable **Two-Factor Authentication**.  

### 4. Limit Lock Screen Access  
- **Why**: Restricts what others can do from the lock screen.  
- **How**:  
  1. Go to **Settings > Face ID & Passcode (or Touch ID & Passcode)**.  
  2. Disable access to **Control Center**, **Siri**, **Reply with Message**, and other features.  

### 5. Secure Your Wi-Fi and Network  
- **Why**: Prevent eavesdropping and data theft.  
- **How**:  
  1. Avoid public Wi-Fi; use a VPN if necessary.  
  2. Use **Settings > Wi-Fi** to ensure your home network uses WPA3 or WPA2 encryption.  

### 6. Enable Find My iPhone  
- **Why**: Helps locate, lock, or erase a lost or stolen iPhone.  
- **How**:  
  1. Go to **Settings > [Your Name] > Find My > Find My iPhone**.  
  2. Enable **Find My iPhone**, **Find My network**, and **Send Last Location**.  

### 7. Restrict App Permissions  
- **Why**: Prevent apps from accessing unnecessary data.  
- **How**:  
  1. Go to **Settings > Privacy & Security**.  
  2. Review permissions (e.g., Location Services, Camera, Microphone) and limit as needed.  

### 8. Disable Ad Tracking  
- **Why**: Enhance privacy by limiting targeted ads.  
- **How**:  
  1. Go to **Settings > Privacy & Security > Tracking**.  
  2. Turn off **Allow Apps to Request to Track**.  

### 9. Use a Secure Backup
- **Why**: Protect backups from unauthorized access.  
- **How**:  
  1. Use **iCloud** with end-to-end encryption enabled.  
  2. Alternatively, use **encrypted local backups** in iTunes/Finder.  

### 10. Install Apps from Trusted Sources Only  
- **Why**: Avoid malware and malicious apps.  
- **How**:  
  1. Only download apps from the Apple App Store.  
  2. Avoid sideloading or jailbreaking your device.  

### 11. Use Safari's Privacy Features  
- **Why**: Protect online activity.  
- **How**:  
  1. Go to **Settings > Safari**.  
  2. Enable **Prevent Cross-Site Tracking**, **Block All Cookies**, and **Fraudulent Website Warning**.  

### 12. Enable Automatic Lock and Erase  
- **Why**: Protect data in case of theft or loss.  
- **How**:  
  1. Go to **Settings > Display & Brightness > Auto-Lock** and set a short duration.  
  2. Go to **Settings > Face ID & Passcode (or Touch ID & Passcode)**.  
  3. Enable **Erase Data** after 10 failed passcode attempts.  

### 13. Turn on Security Recommendations  
- **Why**: Identifies weak passwords and security vulnerabilities.  
- **How**:  
  1. Go to **Settings > Passwords**.  
  2. Review and address any **Security Recommendations**.  

### 14. Use Secure Communication Apps  
- **Why**: Encrypt conversations.  
- **How**:  
  1. Use apps like **iMessage**, **Signal**, or **WhatsApp** for encrypted communication.  

### 15. Monitor Device Analytics and Logs  
- **Why**: Ensure apps and services aren’t accessing unnecessary data.  
- **How**:  
  1. Go to **Settings > Privacy & Security > Analytics & Improvements**.  
  2. Disable options you’re not comfortable with.  

---

## Step-by-Step Guide to Secure an Apple iPhone Managed by an MDM Server  
### 1. Deploy a Compliant MDM Server  
- **Why**: The MDM server enforces DISA STIG policies and configurations remotely.  
- **How**:  
  1. Set up or subscribe to an MDM solution (e.g., MobileIron, Jamf Pro, Itune orVMware Workspace ONE).   

### 2. Enroll iPhones into MDM  
- **Why**: Enables centralized management of devices.  
- **How**:  
  1. Navigate to **Settings > General > Device Management** on the iPhone.  
  2. Follow instructions to enroll the device using an MDM enrollment URL or QR code.  

### 3. Enforce Passcode Policies  
- **Why**: Strengthens access security.  
- **How** (via MDM):  
  - Require:  
    - Minimum 6-digit passcodes.  
    - Maximum passcode age and history.  
    - Auto-lock after inactivity.  
  - Enforce biometric authentication (Face ID or Touch ID).  

### 4. Disable Unapproved Features  
- **Why**: Limits attack vectors.  
- **How** (via MDM):  
  - Disable:  
    - **AirDrop**  
    - **iCloud Backup** if sensitive data should remain on-premises.  
    - **Personal Hotspot**  
    - **Screen Recording**.  

### 5. Enforce Network Security Settings  
- **Why**: Protects data during transmission.  
- **How** (via MDM):  
  1. Configure VPN profiles to secure all network traffic.  
  2. Apply DNS filtering to block malicious domains.  
  3. Restrict connections to approved Wi-Fi networks only.  

### 6. Limit Application Use  
- **Why**: Prevents installation and use of unauthorized apps.  
- **How** (via MDM):  
  1. Use **App Whitelisting** to specify approved applications.  
  2. Block access to the Apple App Store if needed.  
  3. Disable sideloading of apps and jailbreaking attempts.  

### 7. Restrict Data Sharing  
- **Why**: Protects sensitive information.  
- **How** (via MDM):  
  1. Disable options like **Clipboard Sharing** and **Universal Clipboard**.  
  2. Limit file sharing and AirPrint to approved devices.  

### 8. Enforce Encryption Settings  
- **Why**: Ensures data remains secure at rest and in transit.  
- **How** (via MDM):  
  1. Ensure device storage encryption is enabled.  
  2. Require email and file encryption for sensitive data.  

### 9. Enable Device Monitoring  
- **Why**: Helps detect and respond to security incidents.  
- **How** (via MDM):  
  1. Enable logging for device and application activities.  
  2. Monitor for unusual behaviors or policy violations.  

### 10. Configure Automatic Wipe and Lock Policies  
- **Why**: Prevents unauthorized access in case of loss or theft.  
- **How** (via MDM):  
  1. Enable automatic device wipe after a set number of failed passcode attempts.  
  2. Set devices to lock after a short period of inactivity.  

### 11. Apply Regular Compliance Checks  
- **Why**: Ensures ongoing adherence to security policies.  
- **How** (via MDM):  
  1. Schedule automated compliance checks.  
  2. Set up alerts for non-compliance.  
  3. Use reports to track and address issues.  

### 12. Train Users on Security Best Practices  
- **Why**: Reduces risks caused by human error.  
- **How**:  
  1. Educate users on secure device usage and recognizing phishing attempts.  
  2. Provide guidance on handling classified or sensitive information.  

### 13. Review and Update Policies Regularly  
- **Why**: Keeps security measures aligned with evolving threats.  
- **How**:  
  1. Regularly review DISA STIGs for updates.  
  2. Apply necessary changes to the MDM profiles.  

## References
- [iPhone Security Guide](https://github.com/iAnonymous3000/iOS-Hardening-Guide)  
- [DISA STIG Viewer](https://public.cyber.mil/stigs/)  
- [Apple MDM Documentation](https://support.apple.com/guide/mdm/welcome/web)  
- [NIST Mobile Security Standards](https://www.nist.gov/)  
