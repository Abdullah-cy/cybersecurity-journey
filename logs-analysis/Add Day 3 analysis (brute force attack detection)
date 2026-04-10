# Day 3 – Brute Force Attack Detection

## Log Example
Failed password for invalid user admin from 185.234.216.12 port 22 ssh2
Failed password for invalid user admin from 185.234.216.12 port 22 ssh2
Failed password for invalid user admin from 185.234.216.12 port 22 ssh2
Failed password for invalid user admin from 185.234.216.12 port 22 ssh2
Accepted password for user from 185.234.216.12 port 22 ssh2

## Analysis
Multiple failed login attempts for an invalid user (admin) from the same IP address indicate a brute force attack. 
The attacker eventually succeeded in logging in as a valid user from the same IP.

## Conclusion
This indicates a successful brute force attack. 
The attacker failed to access the admin account but managed to gain access to another user account.

## Notes
Brute force attacks involve repeated login attempts to guess credentials.
## Severity
High (multiple failed attempts followed by successful login)

## Recommended Action
- Block the attacking IP address
- Reset the compromised user password
- Investigate account activity
- Enable MFA
