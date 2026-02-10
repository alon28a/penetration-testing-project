# Penetration Testing Project – IP Camera & Vehicle Access

## 📌 Overview
This project was conducted as part of my cybersecurity studies.
The objective was to assess the security of a wireless IP camera system and
identify weaknesses that could allow an attacker to bypass monitoring
mechanisms and gain unauthorized access to a protected asset.

The test was performed in a controlled lab environment for educational purposes only.

## 🎯 Scope
- Target: Wireless IP Camera System
- Testing Type: Black-box
- Attack Surface:
  - Wireless communication
  - Session handling
  - Behavioral workflow enforcement

## 🛠 Tools & Techniques
- Wireless frequency analysis
- Signal capture
- Signal interference (jamming)
- Manual exploitation techniques

## 🔍 Key Findings

### 🔴 Critical – Unsecured Communication
**Description:**  
The system communicates over an unencrypted wireless channel. By tuning into
the correct frequency, it was possible to intercept and capture communication
signals and reuse them to gain unauthorized access.

**Impact:**  
- Unauthorized access to the vehicle
- Session hijacking
- Replay attacks

**Evidence:**  
Access was achieved by identifying the correct frequency and capturing the
transmitted signal without any authentication.

**Remediation:**
- Encrypt communications using TLS/SSL
- Implement secure session tokens with expiration and replay protection

---

### 🟠 High – Signal Jamming
**Description:**  
The IP camera relies on wireless communication (2.4GHz / 5GHz).
By transmitting interference on the operating frequency, the camera could be
rendered temporarily blind.

**Impact:**  
- Camera bypass without authentication
- Loss of video feed and alerts
- Ability to move through monitored areas undetected

**Evidence:**  
By using the correct frequency, camera detection was bypassed and monitoring
was disrupted.

**Remediation:**
- Prefer wired connections where possible
- Implement jamming detection mechanisms
- Monitor abnormal interference levels and generate alerts

## 📊 Risk Assessment
From an overall security perspective, the system was assessed as **Low security maturity**.
The identified vulnerabilities require low technical skill to exploit and have a high potential impact.

## 🧠 Methodology
1. Reconnaissance – Identifying wireless frequencies and communication behavior
2. Vulnerability Identification – Detecting unencrypted communication and weak workflow enforcement
3. Exploitation – Signal capture and jamming
4. Impact Analysis – Bypassing camera detection and gaining access
5. Reporting – Documentation and remediation recommendations

## ⚠️ Disclaimer
This project was performed in a controlled environment as part of academic studies.
No real-world systems were harmed or accessed illegally.
