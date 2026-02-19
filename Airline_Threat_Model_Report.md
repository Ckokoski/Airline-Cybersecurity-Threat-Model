# Airline Cybersecurity Threat Model Report

## Environment Overview

A commercial airline operates a hybrid environment combining corporate IT, customer-facing systems, and operational technology (OT). Unlike most organizations, availability and safety are critical requirements.

Primary system categories:

1. Passenger Systems
2. Airport Networks
3. Operational Technology
4. Aircraft Communications
5. Vendor Integrations
6. Employee Identity Infrastructure

---

## Key Assets

- Passenger Personally Identifiable Information (PII)
- Payment Card Data
- Flight Operations Systems
- Aircraft Dispatch Communications
- Loyalty Program Accounts
- Employee Credentials

---

## Threat Actors

### Cybercriminals
Goal: financial fraud, ransomware, account takeover

### Nation-State Actors
Goal: disruption, intelligence gathering, transportation impact

### Insider Threats
Goal: data theft, sabotage, credential misuse

### Hacktivists
Goal: public disruption and reputational damage

---

## Attack Surface Analysis

### 1. Passenger Reservation System
Risks:

- Credential stuffing
- Loyalty account takeover
- Payment fraud

Impact:
Financial loss, brand damage, customer lawsuits

Detection:

- Login anomaly detection
- Geographic login mismatch
- Failed authentication spikes

---

### 2. Airport Wi-Fi Networks
Risks:

- Rogue access points
- Man-in-the-middle attacks
- Session hijacking

Impact:
Credential theft, malware delivery

Detection:

- Wireless intrusion detection
- DHCP anomalies
- ARP spoofing alerts

---

### 3. Baggage Handling System (Operational Technology)
Risks:

- Ransomware
- PLC manipulation
- Network pivot to corporate network

Impact:
Airport shutdown, flight delays

Detection:

- Network segmentation monitoring
- ICS traffic anomalies
- Unauthorized SMB traffic

---

### 4. Mobile Airline App
Risks:

- API abuse
- Token theft
- Data scraping

Impact:
Mass account compromise

Detection:

- API rate monitoring
- Token reuse detection
- Unusual device fingerprinting

---

### 5. Vendor Integrations
Risks:

- Supply chain compromise
- Compromised maintenance vendors

Impact:
Large-scale breach

Detection:

- Vendor VPN monitoring
- After-hours access alerts
- Privileged activity logging

---

## Recommended Security Controls

- Multi-factor authentication for all employee access
- Network segmentation between IT and OT systems
- SIEM monitoring of authentication logs
- Endpoint detection and response (EDR)
- Vendor access restrictions
- Security awareness training for phishing resistance
