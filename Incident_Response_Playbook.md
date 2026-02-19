# Airline Security Incident Response Playbook

## Phishing Incident

### Detection Triggers
- User reports suspicious email
- Email security gateway alert
- Multiple users receive identical message
- Suspicious login shortly after email delivery

### Triage (First 10 Minutes)
1. Obtain a copy of the email (headers + body)
2. Identify sender domain and reply-to address
3. Check if links or attachments were accessed
4. Search SIEM for additional recipients
5. Review authentication logs for affected users

### Immediate Containment
- Block sender domain in email gateway
- Disable compromised accounts
- Revoke active sessions
- Reset user passwords
- Remove email from all mailboxes if possible

### Investigation
- Analyze email headers for spoofing
- Check URL reputation
- Determine credential harvesting vs malware delivery
- Identify patient zero (first compromised account)

### Escalation
Escalate to Security Lead if:
- Privileged account accessed
- Multiple accounts compromised
- External data accessed

### Communication
- Notify IT Help Desk
- Notify affected users
- Document incident in ticketing system


---

## Ransomware Detection

### Detection Triggers
- EDR alert for mass file encryption
- Unusual file rename activity
- Users report inaccessible files
- Suspicious PowerShell or admin tool execution
- Sudden spike in SMB traffic

### Triage (First 10 Minutes)
1. Identify the affected host(s)
2. Determine if encryption is still active
3. Check for lateral movement indicators
4. Review recent login activity
5. Identify the user account associated with the system

### Immediate Containment
- Isolate infected workstation from network
- Disable associated user accounts
- Block suspected command-and-control IP addresses
- Stop shared drive access if necessary

### Investigation
- Review EDR telemetry for initial entry vector
- Check email logs for phishing delivery
- Determine if domain admin privileges were used
- Identify patient zero system

### Escalation
Escalate immediately if:
- Domain controller activity observed
- Multiple hosts infected
- Backup systems accessed

### Recovery
- Reimage affected systems
- Restore from clean backups
- Rotate privileged credentials
- Monitor network for reinfection

### Communication
- Notify IT leadership
- Notify affected departments
- Document incident and timeline


---

## Compromised Vendor Account

### Detection Triggers
- Vendor login outside normal hours
- Login from foreign or unusual geographic location
- Access to systems not normally used by vendor
- Large data transfers

### Triage (First 10 Minutes)
1. Identify vendor account activity
2. Confirm vendor’s normal access schedule
3. Review authentication logs
4. Check accessed systems and files

### Immediate Containment
- Disable vendor VPN account
- Revoke active sessions
- Block suspicious IP addresses
- Temporarily suspend vendor access

### Investigation
- Determine accessed systems
- Check for data exfiltration
- Review privileged actions
- Verify vendor system compromise

### Escalation
Escalate if:
- Sensitive data accessed
- Administrative systems accessed
- Persistence mechanisms detected

### Communication
- Notify vendor security contact
- Notify internal security management
- Document incident findings
