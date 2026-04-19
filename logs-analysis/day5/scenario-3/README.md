# Day 5 – Scenario 3

## Log Example

```
Accepted password for user dev from 192.168.1.15 port 22 ssh2
user executed command: sudo su
user is now root
user created new account: test_admin
user added cron job: /var/tmp/update.sh every 10 minutes
connection from 192.168.1.15 to 192.168.1.30 via SSH
connection from 192.168.1.30 to 192.168.1.50 via SSH
```

---

## Log Explain

- Successful login for user "dev" from internal IP address (192.168.1.15)
- dev executed communed to git root access
- sucssful access root user
- the root created account (test_admin)
- a cron job was added (`/var/tmp/update.sh`) every 10 minutes
- connection from ip adders to anther ip adders
- anther connection to ip adders


## Analysis
The activity begins with a successful login from an internal IP address, which may indicate a compromised internal host.

The user "dev" escalated privileges to root using "sudo su", indicating privilege escalation.

After gaining root access, the attacker created a new account (test_admin), which may serve as a persistence mechanism.

Additionally, a cron job was added to execute a script every 10 minutes, further ensuring persistence.

The attacker then moved laterally within the network, connecting from 192.168.1.15 to 192.168.1.30, and then to 192.168.1.50 via SSH, indicating active spread inside the network.

## Key Indicators
- Successful login from internal IP
- Privilege escalation to root
- Creation of unauthorized account (test_admin)
- Persistence via cron job (/var/tmp/update.sh)
- Multiple lateral movement activities via SSH
  
## Possible Threat
- Privilege Escalation Attack
- Persistence Mechanism (cron job + account creation)
- Lateral Movement Attack
- Full System Compromise


## MITRE ATT&CK Mapping
- T1136 → Create Account
- T1059 → Command Execution
- T1078 → Valid Accounts
- T1053 → Cron Job
- T1021 – Remote Services


## Conclusion

This is a confirmed active attack involving privilege escalation, persistence, and lateral movement. The attacker has likely achieved full system compromise.


## Severity

Critical
(Internal access + root privileges + lateral movement)


## Recommended Action
- Isolate the affected host from the network
- Remove unauthorized accounts (test_admin)
- Delete malicious cron jobs and scripts
- Investigate lateral movement to other systems
- Reset credentials for compromised accounts
- Enable MFA




## Notes

*
