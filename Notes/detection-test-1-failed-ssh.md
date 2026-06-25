## Detection Test 1: Failed SSH Login

**Source:** Wazuh server  
**Target:** Linux endpoint  
**Target IP:** 172.19.13.246  
**Tool/Service:** SSH  
**Log Source:** /var/log/auth.log  
**Detection Platform:** Wazuh  

### Activity Performed
I attempted several SSH logins using an invalid username and incorrect passwords.

### Result
Wazuh generated authentication failure alerts from the Linux endpoint.

### Security Relevance
Repeated failed SSH logins can indicate brute-force activity, password guessing, or unauthorized access attempts.

### Evidence
Screenshot: screenshots/03-linux-failed-ssh-alert.png
