## Detection Test 3: Nmap Scan Before Hardening

**Source:** Wazuh server  
**Target:** Linux endpoint  
**Target IP:** 172.30.92.148  
**Tool/Service:** Nmap  
**Log Source:** Nmap scan output and Wazuh network/security events if generated  
**Detection Platform:** Wazuh  

### Activity Performed
I ran an Nmap scan from the Wazuh server against the Linux endpoint to identify exposed ports and running services before applying hardening controls.

### Result
Nmap identified the services exposed on the Linux endpoint. The scan provided a baseline view of the system’s attack surface before remediation.

### Security Relevance
Port and service discovery helps security engineers identify unnecessary exposed services, validate firewall rules, and reduce attack surface. This is a common first step in vulnerability management and host hardening.

### Evidence
Screenshot: screenshots/05-nmap-scan-before-hardening.png  
Scan Output: linux-endpoint-service-scan-before.txt
