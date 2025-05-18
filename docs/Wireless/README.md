# Microsoft NPS with Meraki Wireless for Domain-Joined Computers

## **1️⃣ Setup Certificate Services and Auto-Enrollment:**
1. Install **Active Directory Certificate Services (AD CS)** on your Windows Server.
2. Configure it as an **Enterprise CA** and enable **Certificate Templates**.
3. Use the **Computer template** for issuing certificates.
   - Open the **Certification Authority** MMC → Right-click **Certificate Templates** → **Manage**.
   - Duplicate the **Computer** template → Name it (e.g., "Domain Computer Wireless").
   - Go to the **Security** tab:
     - Allow **Domain Computers** to **Enroll** and **Auto-enroll**.
4. Publish the template:
   - Right-click **Certificate Templates** → **New** → **Certificate Template to Issue** → Select your newly created template.

5. Configure **Group Policy** for auto-enrollment:
   - Go to **Group Policy Management** → Create a new GPO or edit an existing one.
   - Navigate to:
     ```
     Computer Configuration → Policies → Windows Settings → Security Settings → Public Key Policies → Certificate Services Client – Auto-Enroll
     ```
   - Enable **Configuration Model: Enabled** and check:
     - Renew expired certificates, update pending certificates, and remove revoked certificates.
     - Update certificates that use certificate templates.

---

## **2️⃣ Configure NPS for Certificate-Based Authentication:**
1. Open **NPS Console** → **RADIUS Clients and Servers** → Add your Meraki AP as a **RADIUS Client**.
2. Go to **Policies** → **Network Policies** → Create a new policy.
3. Define the **Conditions**:
   - **NAS Port Type** → Select **Wireless - IEEE 802.11**.
   - **Windows Groups** → Add **Domain Computers**.
4. **Constraints**:
   - Select **Authentication Methods** → **Smart Card or other certificate**.
   - Click **Configure** → **EAP Types** → **Add** → **Microsoft: Smart Card or other certificate**.
5. Under **Settings** → **Encryption**:
   - Ensure **Strongest encryption** options are selected (AES, SHA256).

---

## **3️⃣ Configure Meraki Wireless for RADIUS Authentication:**
1. Log in to the **Meraki Dashboard** → **Wireless** → **Access Control**.
2. Under **SSID** settings, choose **Enterprise with RADIUS**.
3. Add your NPS server as the **RADIUS Server**:
   - **RADIUS IP**: `<NPS Server IP>`
   - **Port**: `1812` (default)
   - **Shared Secret**: `<Configured in NPS>`
4. Enable **802.1X Authentication** → Choose **PEAP (MS-CHAP v2)**.
5. Ensure **WPA2-Enterprise** is selected.

---

## **4️⃣ Validate Certificate-based Authentication:**
1. On a domain-joined computer, open **MMC** → **Certificates** → **Computer Account** → **Personal** → **Certificates**.
2. Ensure the **Domain Computer Wireless** certificate is present and valid.
3. Attempt to connect to the Meraki SSID.
4. The NPS server will validate:
   - The client is domain-joined (part of **Domain Computers** group).
   - The certificate is signed by the AD CS.
   - The client is authorized through NPS policies.

---

## **5️⃣ Optional Security Hardening:**
1. Restrict NPS policy to specific **OU**s if necessary.
2. Use **Certificate Revocation Lists (CRL)** to prevent compromised machines from authenticating.
3. Enforce **Group Policy** to only allow **domain-certified networks**.


## Guide to Securing Enterprise Wireless Access Points  
Securing enterprise wireless access points (APs) is essential for protecting network resources and sensitive data. Below is a step-by-step guide with references to industry best practices.  

### 1. Implement WPA3 Encryption  
   - **Step**: Configure all wireless access points to use WPA3 for authentication and encryption.  
   - **Why**: WPA3 offers stronger security than its predecessors, including protections against brute-force attacks.  
   - **Sources**:  
     - [Wi-Fi Alliance - WPA3](https://www.wi-fi.org/discover-wi-fi/security)  

### 2. Use a Robust Authentication Mechanism  
   - **Step**: Deploy an 802.1X authentication framework with RADIUS server integration.  
   - **Why**: 802.1X provides enterprise-grade access control and prevents unauthorized access.  
   - **How**:  
     - Install a RADIUS server (e.g., FreeRADIUS).  
     - Integrate with Active Directory or LDAP.  
   - **Sources**:  
     - [FreeRADIUS Deployment Guide](https://www.freeradius.org/documentation/freeradius-server/3.2.7/)  

### 3. Segment and Isolate Wireless Networks  
   - **Step**: Create VLANs to segment guest, employee, and IoT traffic.  
   - **Why**: Limits the spread of attacks and isolates sensitive data.  
   - **Sources**:  

### 4. Enable Access Point Management Security  
   - **Step**:  
     - Change default credentials for AP management interfaces.  
     - Use HTTPS and disable insecure protocols (e.g., Telnet).  
   - **Why**: Prevents unauthorized access to management interfaces.  
   - **Sources**:  
     - [NIST SP 800-153 Wireless Security Guidelines](https://csrc.nist.gov/publications/detail/sp/800-153/final)  

### 5. Implement Network Monitoring and Intrusion Detection  
   - **Step**: Deploy wireless intrusion detection/prevention systems (WIDS/WIPS) to detect rogue access points and anomalous activity.  
   - **Why**: Provides real-time threat detection and mitigation.  
   - **Sources**:   

### 6. Regularly Update Firmware and Software  
   - **Step**: Schedule regular updates for AP firmware and related network software.  
   - **Why**: Fixes known vulnerabilities and enhances performance.  
   - **Sources**:  

### 7. Restrict Physical Access to Wireless Access Points  
   - **Step**:  
     - Secure APs in tamper-proof enclosures.  
     - Limit access to authorized personnel.  
   - **Why**: Prevents unauthorized tampering or device theft.  
   - **Sources**:  

### 8. Deploy Strong Network Policies  
   - **Step**: Enforce policies such as:  
     - Disabling SSID broadcasting for private networks.  
     - Using MAC address filtering sparingly (not a primary security measure).  
   - **Why**: Ensures controlled access to the network.  
   - **Sources**:   

### 9. Educate Users  
   - **Step**: Train employees on secure Wi-Fi usage and phishing awareness.  
   - **Why**: Reduces risk from human error and social engineering attacks.  
   - **Sources**:  
     - [SANS Security Awareness Training](https://www.sans.org/security-awareness-training/)  

### 10. Perform Regular Security Testing  
   - **Step**: Conduct penetration testing to identify vulnerabilities and validate security measures.  
   - **Why**: Helps maintain a proactive security posture.  
   - **Sources**:  
     - [OWASP Wireless Testing Guide](https://owasp.org/www-project-mobile-security-testing-guide/)  

By following these steps and leveraging the provided resources, you can significantly enhance the security of your enterprise wireless network.  

## References  
- [Dod STIG](https://www.stigviewer.com/stig/network_wlan_ap-ig_management/)  