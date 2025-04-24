# FUTIRE_CS_03
**Wi-Fi Security Assessment Report**

**Project Title:** Home Network Security Evaluation
**Tester:** Anish aka Mr.WHite
**Date:** April 24, 2025
**Target:** Home Wi-Fi Network (SSID: "HomeNet_24")
**Tools Used:** Wireshark, Aircrack-ng, Nmap
**Objective:** To identify vulnerabilities in the home Wi-Fi network and recommend measures to strengthen overall wireless security.

---

## 1. Objective
The objective of this assessment was to perform a thorough security analysis of a residential Wi-Fi network. The assessment focused on identifying weak encryption, insecure device configurations, open ports, and unauthorized devices connected to the network.

---

## 2. Methodology

1. **Network Scanning:** Using Nmap to detect active devices and open ports.
2. **Packet Analysis:** Using Wireshark to inspect traffic and look for unencrypted data or suspicious activity.
3. **Wi-Fi Security Testing:** Using Aircrack-ng to assess encryption strength and test for weak or default passwords.

---

## 3. Tools Used

### Wireshark
- Network protocol analyzer
- Used to capture and analyze packets on the Wi-Fi network
- Checked for data leakage or plaintext credentials

### Aircrack-ng
- Wireless security auditing tool
- Used to analyze WPA/WPA2 handshake captures
- Performed password strength testing and dictionary attacks

### Nmap
- Network scanner
- Identified connected devices, open ports, and running services

---

## 4. Assessment Results

### A. Device Discovery (via Nmap)
- Total devices detected: 9
- 2 unknown devices with suspicious MAC addresses found
- Open ports detected:
  - Port 23 (Telnet) on a smart TV – considered insecure
  - Port 80 (HTTP) on IP Camera – no password protection

### B. Traffic Analysis (via Wireshark)
- No HTTPS on certain smart home devices
- Detected multiple plaintext HTTP sessions
- Some DNS queries leaked metadata about browsing habits

### C. Wi-Fi Security Testing (via Aircrack-ng)
- Encryption Type: WPA2-PSK
- Password Crack Time (with dictionary): ~35 minutes
- Password used: "home1234" – weak, dictionary word

---

## 5. Risk Analysis

- **Weak Password:** Easily guessable or crackable Wi-Fi password.
- **Insecure Ports:** Telnet and HTTP open without protection.
- **Unknown Devices:** Potential unauthorized access.
- **Metadata Leakage:** DNS and HTTP activity visible to attackers on network.

---

## 6. Recommendations

1. **Update Wi-Fi Password:** Use a strong, unique password (min. 12 characters, mixed case, symbols).
2. **Device Audit:** Remove or verify all unknown devices.
3. **Disable Insecure Services:** Turn off Telnet, or replace with SSH where needed.
4. **Use HTTPS-Only Devices:** Replace or update devices that only use HTTP.
5. **Enable Guest Network:** Isolate guest devices from main network.
6. **Enable WPA3 (if supported):** Stronger encryption for modern devices.
7. **Regular Monitoring:** Schedule monthly scans with Nmap and occasional packet captures.

---

## 7. Conclusion
The assessment highlighted several security concerns within the home Wi-Fi network, particularly around weak encryption practices, insecure services, and unauthorized devices. Applying the listed recommendations will significantly improve network resilience against common threats.

---

**End of Report**

