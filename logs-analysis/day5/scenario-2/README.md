# Day 5 – Scenario 2

## Log Example

```
Failed password for user admin from 185.220.101.45 port 22 ssh2
Failed password for user admin from 185.220.101.45 port 22 ssh2
Failed password for user admin from 185.220.101.45 port 22 ssh2
Accepted password for user admin from 185.220.101.45 port 22 ssh2
user executed command: sudo su
user is now root
user modified file: /etc/passwd
user added SSH key to /root/.ssh/authorized_keys
```

---

## Log Explain

* Multiple failed login attempts from external IP (185.220.101.45)
* Successful login using valid credentials
* User executed "sudo su" to escalate privileges
* User gained root access
* System file (/etc/passwd) was modified
* SSH key added to root authorized_keys file

---

## Analysis

The repeated failed login attempts indicate a brute force attack. The attacker eventually gained access using valid credentials.

After login, the attacker escalated privileges to root. Modifying the `/etc/passwd` file is highly critical and may indicate account manipulation.

Adding an SSH key to `/root/.ssh/authorized_keys` establishes persistence, allowing the attacker to reconnect without a password.

---

## Key Indicators

* Multiple failed login attempts (brute force)
* Successful login from external IP
* Privilege escalation to root
* Modification of critical system file (/etc/passwd)
* Persistence via SSH key

---

## Possible Threat

* Brute Force Attack
* Account Compromise
* Privilege Escalation
* Persistence Mechanism
* Full System Compromise

---

## MITRE ATT&CK Mapping

* T1110 – Brute Force
* T1078 – Valid Accounts
* T1059 – Command Execution
* T1098 – Account Manipulation

---

## Conclusion

This is a confirmed attack involving brute force, account compromise, privilege escalation, and persistence. The attacker has likely achieved full system control.

---

## Severity

Critical
(External access + root privileges + persistence)

---

## Recommended Action

* Block the attacking IP address
* Reset compromised account credentials
* Remove unauthorized SSH keys
* Restore integrity of /etc/passwd
* Enable MFA
* Monitor for further suspicious activity

---

## Notes

* External attacker gained full access
* High risk of persistent access via SSH key
