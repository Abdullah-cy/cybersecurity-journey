# Lab: Detect Suspicious Activity

## Platform
TryHackMe

## Objective
Identify suspicious activity and respond to the attack.

## Detection
A web discovery attack was detected from an external IP address.

## Findings
- Source IP: 32.122.195.63
- Attack type: Directory Enumeration
- Targeted endpoints:
  - /admin
  - /login
  - /wp-admin
  - /administrator

## Analysis
The attacker attempted multiple requests to different admin-related endpoints.

This behavior indicates automated directory enumeration using tools such as:
- dirb
- gobuster
- dirbuster

The goal is to discover hidden or sensitive pages.

## Response (Containment)
The attacker's IP address (32.122.195.63) was blocked using a firewall rule.

## Result
- Attack stopped
- Malicious traffic blocked

## MITRE ATT&CK Mapping
- T1595 (Active Scanning)
