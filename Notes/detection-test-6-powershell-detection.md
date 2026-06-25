## Detection Test 6: Suspicious PowerShell Execution

**Source:** Windows endpoint  
**Target:** Windows endpoint  
**Target IP:** <WINDOWS_ENDPOINT_IP>  
**Tool/Service:** PowerShell, Sysmon  
**Log Source:** Microsoft-Windows-Sysmon/Operational, Sysmon Event ID 1  
**Detection Platform:** Wazuh  

### Activity Performed
I executed a safe encoded PowerShell command on the Windows endpoint to simulate suspicious command-line behavior commonly monitored in enterprise environments.

### Result
Sysmon captured the PowerShell process creation event. Wazuh ingested the Windows telemetry and displayed the PowerShell activity in the security events dashboard.

### Security Relevance
Encoded PowerShell commands can be used by attackers to hide malicious activity, evade simple command-line inspection, or execute payloads. Monitoring encoded PowerShell execution helps security teams detect suspicious endpoint behavior.

### Evidence
Screenshot: screenshots/11-powershell-encodedcommand-alert.png