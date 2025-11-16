# Email Phishing Investigation in Healthcare

**Author: [Adams Samson](https://www.linkedin.com/in/adams-samson) · [GitHub](https://github.com/adamssamson)**

This case study explores a real-world phishing incident targeting **Health Guard Medical Network**, a leading healthcare provider in California. It outlines the detection, analysis, and response strategies used to mitigate the threat and strengthen the organization’s cybersecurity posture.

---

## Incident Overview

- **Phishing Email**: Spoofed Microsoft alert from `no-reply@access-accsecurity.com`  
- **Malicious Link**: Redirected to `https://sign.in/`  
- **Delivery Time**: August 16, 2023, 00:15 AM  

---

## Technical Analysis

### Email Authentication Failures

-  SPF failed: sender IP not authorized  
-  No DKIM signature  
-  Invalid DMARC policy  

### Threat Intelligence

-  **VirusTotal** flagged the URL as phishing  
-  **PhishTool** confirmed spoofed branding and urgency-driven language  

### Log Analysis via Splunk

-  Suspicious login activity from `alice@`, `bob@`, and `carol@healthguardmed.net`  
-  Logins occurred shortly after phishing email delivery  

---

## Risk Assessment

| Risk Factor              | Impact                              |
|--------------------------|--------------------------------------|
| Unauthorized EHR Access  | High                                 |
| HIPAA Non-Compliance     | Severe fines, legal exposure         |
| Loss of Patient Trust    | Long-term reputational damage        |
| Operational Disruption   | Delays in care and system downtime   |

---

## Response & Mitigation

### Immediate Actions

-  Blocked domain `access-accsecurity.com` and IP `89.144.44.41`  
-  Isolated affected accounts and reset credentials  
-  Monitored outbound traffic for data exfiltration  

### Long-Term Measures

-  Enforced Multi-Factor Authentication (MFA)  
-  Upgraded email filtering and sandboxing  
-  Conducted regular phishing simulations  

---

## Training & Awareness

Health Guard launched targeted training modules and a comprehensive awareness guide to reinforce key security practices across the organization.

---

## Outcome

- No confirmed compromise  
-  Improved security posture  
-  Reinforced commitment to HIPAA compliance and patient data protection  

---

##  Next Steps

-  Continuous monitoring  
-  Expanded phishing simulations  
-  Review and optimize email gateway configurations  

