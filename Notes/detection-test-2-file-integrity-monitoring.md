## Detection Test 2: File Integrity Monitoring

**Source:** Linux endpoint  
**Target:** Linux endpoint  
**Target IP:** 172.30.92.148  
**Tool/Service:** Wazuh File Integrity Monitoring  
**Log Source:** /var/ossec/logs/ossec.log and Wazuh syscheck events  
**Detection Platform:** Wazuh  

### Activity Performed
I configured Wazuh to monitor the `/secure-data` directory on the Linux endpoint. I then modified the file `/secure-data/important.conf` to simulate an unauthorized configuration change.

### Result
Wazuh generated a file integrity monitoring alert showing that the monitored file was modified.

### Security Relevance
File integrity monitoring helps detect unauthorized changes to sensitive files, configuration files, scripts, and system directories. This is useful for identifying suspicious activity, persistence attempts, or accidental misconfigurations.

### Evidence
Screenshot: screenshots/04-file-integrity-monitoring-alert.png