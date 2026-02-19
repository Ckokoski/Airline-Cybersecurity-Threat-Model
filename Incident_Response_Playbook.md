# Airline Security Incident Response Playbook

## Phishing Incident

1. User reports suspicious email
2. SOC analyzes email headers and links
3. Block sender domain
4. Reset affected credentials
5. Search SIEM for additional victims
6. Notify affected users

---

## Ransomware Detection

1. EDR detects encryption behavior
2. Isolate the infected workstation
3. Disable affected accounts
4. Identify lateral movement
5. Restore from backup
6. Conduct root cause analysis

---

## Compromised Vendor Account

1. Detect unusual login time or location
2. Disable vendor VPN account
3. Review access logs
4. Verify vendor system integrity
5. Rotate credentials
6. Notify vendor security contact
