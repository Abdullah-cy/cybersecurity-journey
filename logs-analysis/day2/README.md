# Day 2 - A successful login is not always safe.

## Log Example
Accepted password for user from 192.168.1.10 port 22 ssh2

## Analysis
This log shows a successful SSH login.

However, a successful login is not always safe.
It could indicate unauthorized access if:
- We cannot determine if the IP address is unusual due to lack of context.
- The login time is not provided
- There is no information about previous failed attempts
## Conclusion
Based on this log alone, we cannot confirm whether the login is legitimate.
Further investigation is required.
## Notes
SSH (Secure Shell) is used for secure remote access.
SSH runs on port 22.
## Severity
Low (single attempt) / Medium-High (if repeated)

## Recommended Action
- Verify if the IP address is trusted
- Check previous login attempts
- Monitor user activity after login
- Enable MFA if not already enabled
