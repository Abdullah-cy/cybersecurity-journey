# Day 1 - Log Analysis Basics
## Log Example
Failed password for root from 192.168.1.10 port 22 ssh2

## Analysis
This log shows a failed login attempt on SSH.

## Conclusion
This could indicate a brute force attack if multiple failed attempts are observed.
## Notes
SSH runs on port 22.
## Severity
Low (single attempt) / Medium-High (if repeated)

## Recommended Action
Monitor for multiple failed login attempts within a short time frame.
Block the source IP if a brute force pattern is confirmed.
