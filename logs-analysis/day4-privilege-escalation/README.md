# Day 4 – Privilege Escalation After SSH Login

## Log Example
Accepted password for user ahmed from 45.77.12.90 port 22 ssh2  
user executed command: sudo su  
user is now root  

---

## Analysis
Due to lack of context, we cannot confirm if the login is legitimate.  
However, the sequence of events (successful SSH login followed by privilege escalation to root) is highly suspicious and may indicate a compromised account or malicious activity.

---

## Key Indicators
- Successful SSH login  
- Execution of "sudo su"  
- User switched to root privileges  
- Suspicious sequence of actions  

---

## Possible Threat
- Privilege Escalation Attack  
- Account Compromise  
- Unauthorized Root Access  
- Potential Persistence or Backdoor Installation  

---

## Conclusion
This activity is highly suspicious and likely indicates a security incident involving privilege escalation. Further investigation is required to determine if it is malicious or legitimate administrative activity.

---

## Severity
High / Critical (Privilege escalation leading to root access)

---

## Recommended Action
- Block the attacking IP address  
- Reset the compromised user password  
- Review and audit account activity  
- Scan the system for backdoors or persistence mechanisms  
- Revoke unnecessary root privileges  
- Isolate the affected system if needed  
- Enable MFA  

---

## Notes
- Root access significantly increases the risk level  
- Lack of context requires cautious investigation  
- Sequence-based detection is critical in identifying threats  
