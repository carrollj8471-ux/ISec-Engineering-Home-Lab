## Detection Test 5: Windows Endpoint Monitoring and Sysmon Installation

**Source:** Windows endpoint  
**Target:** Windows endpoint  
**Target IP:** **********  
**Tool/Service:** Wazuh Agent, Sysmon, Windows Event Logs  
**Log Source:** Windows Event Logs and Microsoft-Windows-Sysmon/Operational  
**Detection Platform:** Wazuh  

### Activity Performed
I installed the Wazuh agent on the Windows endpoint and configured it to communicate with the Wazuh server. I then installed Sysmon to improve Windows endpoint telemetry and generate detailed security events such as process creation and system activity.

### Result
The Windows endpoint successfully connected to the Wazuh dashboard as an active agent. Sysmon was installed and began writing events to the Microsoft-Windows-Sysmon/Operational event log.

### Security Relevance
Windows endpoint monitoring is critical for detecting suspicious activity such as failed logins, process execution, PowerShell usage, persistence attempts, and lateral movement. Sysmon improves visibility by collecting detailed endpoint telemetry that is useful for threat detection and incident response.

### Evidence
Screenshot: screenshots/08-windows-agent-connected.png  
Screenshot: screenshots/09-sysmon-installed.png