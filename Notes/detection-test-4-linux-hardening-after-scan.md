## Detection Test 4: Linux Hardening and After Scan

**Source:** Wazuh server  
**Target:** Linux endpoint  
**Target IP:** 172.30.92.148  
**Tool/Service:** UFW, SSH, Nmap  
**Log Source:** Nmap scan output and Linux firewall configuration  
**Detection Platform:** Wazuh  

### Activity Performed
I reviewed the exposed services on the Linux endpoint and identified that SSH was visible before hardening. I then enabled the UFW firewall and applied host-level hardening to reduce the system’s exposed attack surface.

### Result
Before hardening, Nmap identified SSH running on port 22. After enabling firewall controls, the follow-up Nmap scan showed all scanned ports as filtered.

### Security Relevance
Reducing exposed services helps limit the attack surface of a system. Firewall enforcement and service restriction are important security engineering controls because they reduce opportunities for unauthorized access, brute-force attempts, and network-based reconnaissance.

### Evidence
Screenshot: screenshots/06-ufw-firewall-enabled.png  
Screenshot: screenshots/07-nmap-scan-after-hardening.png  
Scan Output: scan-results/linux-endpoint-service-scan-before.txt  
Scan Output: scan-results/linux-endpoint-service-scan-after.txt