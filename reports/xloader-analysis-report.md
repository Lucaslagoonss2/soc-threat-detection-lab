# XLoader Malware Traffic Analysis Report

## Overview

This investigation analyzed suspicious network traffic associated with a potential XLoader malware infection using Wireshark in a controlled lab environment

The objective was to identify Indicators of Compromise (IOCs), suspicious communications, and malware-related behavior through packet analysis

---

# Investigation Summary

The infected host generated suspicious DNS requests and external HTTP communications with potentially malicious infrastructure

The traffic analysis revealed encoded GET requests, external TCP communications, and JavaScript redirect behavior commonly associated with malware delivery or callback activity

---

# Identified Indicators of Compromise (IOCs)

## Suspicious Domains

- www.physicsbrain.xyz
- www.satoshichecker.xyz
- www.woca.group

---

## Suspicious IP Address

- 76.223.54.146

---

# Observed Activity

- Suspicious DNS queries
- External TCP communication
- HTTP GET requests with encoded parameters
- JavaScript redirect behavior
- Potential malware callback traffic

---

# HTTP Stream Findings

The HTTP stream analysis identified suspicious requests involving encoded parameters and redirect behavior

Example observed request:

```http
GET /pzee/?GA=...
Host: www.woca.group
```

Observed response behavior:

```javascript
window.location.href="/lander?GA=..."
```

This activity may indicate:
- Malware callback communication
- Redirect-based payload delivery
- Suspicious web infrastructure
- Traffic distribution behavior

---

# Tools Used

- Wireshark
- Kali Linux
- TCP/IP Analysis
- DNS Analysis
- HTTP Stream Inspection

---

# Conclusion

The investigation successfully identified suspicious network behavior consistent with malware-related activity associated with XLoader infection traffic

The analysis demonstrated practical SOC investigation techniques including DNS analysis, IOC extraction, HTTP traffic inspection, and malware communication analysis
