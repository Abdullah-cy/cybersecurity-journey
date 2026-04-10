# Day 4 - part 1 – Suspicious Login Detection

## Log Example
Accepted password for user ahmed from 45.77.12.90 port 22 ssh2

## Analysis
A successful login occurred for user "ahmed" from IP address 45.77.12.90.

However:
- The IP address is unfamiliar / not trusted
- The login time may be unusual (e.g., late night)
- No prior activity from this IP

This could indicate:
- Account compromise
- Unauthorized access using stolen credentials
- Login from attacker using VPN

## Conclusion
Although the login was successful, it is considered suspicious due to abnormal context (unknown IP / unusual behavior).

## Notes
Successful login does NOT always mean safe activity.

## Severity
Medium to High (depending on context)

## Recommended Action
- Verify user activity
- Check login history
- Enable MFA if not enabled
- Alert the user
- Monitor for further suspicious actions
