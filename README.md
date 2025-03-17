# Evil Twin Attack: A Comprehensive Guide

<!--![Evil Twin Attack Banner](https://www.stationx.net/wp-content/uploads/2023/07/evil-twin-WiFi-attack-featured-image.png)-->
<img src="https://www.stationx.net/wp-content/uploads/2023/07/evil-twin-WiFi-attack-featured-image.png" width="1000" height="400" alt="Evil Twin Attack Banner">
Image source: www.stationx.net


**Evil Twin Attacks** exploit human trust in familiar Wi-Fi networks to steal sensitive data. This guide explains how these attacks work, how to detect them, and best practices for prevention.

---

## Table of Contents
1. [What is an Evil Twin Attack?](#what-is-an-evil-twin-attack)
2. [Step-by-Step Explanation](#step-by-step-explanation)
3. [Why Are Evil Twin Attacks Dangerous?](#why-are-they-dangerous)
4. [Detection Techniques](#how-to-detect)
5. [Prevention Measures](#prevention)
6. [Real-Life Examples](#examples)
7. [Ethical Testing & Tools](#tools)
8. [References](#references)
9. [Contribute](#contribute)

---

## <a name="what-is-an-evil-twin-attack"></a>What is an Evil Twin Attack?
An **Evil Twin Attack** involves creating a rogue Wi-Fi access point that mimics a legitimate network. Users unknowingly connect to this fake network, allowing attackers to:
- Intercept sensitive data (passwords, credit card details).
- Monitor browsing activity.
- Inject malware or phishing content.

---

## <a name="step-by-step-explanation"></a>Step-by-Step Explanation

### 1. Setup of the Rogue Access Point
- **Tools Used**: `Wi-Fi Pineapple`, `hostapd-wpe`, or `aircrack-ng`.
- **Techniques**:
  - Clone the legitimate SSID (e.g., "Starbucks_Free_WiFi").
  - Spoof the MAC address of the real access point.
  - Broadcast a stronger signal to attract victims.

### 2. Deception and Victim Connection
- **Lure Tactics**:
  - Position closer to victims for a stronger signal.
  - Launch a DoS attack on the legitimate network to force reconnection.
- **Device Behavior**: Most devices auto-connect to stronger signals with familiar SSIDs.

### 3. Captive Portal Setup
- **Tools**: `dnsmasq`, `Fluxion`.
- **Fake Login Pages**: Mimic legitimate portals (e.g., hotel or café login screens).

### 4. Data Interception and Exploitation
- **MitM Techniques**:
  - Use `Wireshark` or `BetterCAP` to capture unencrypted traffic.
  - Redirect users to phishing sites (e.g., fake banking pages).

---

## <a name="why-are-they-dangerous"></a>Why Are Evil Twin Attacks Dangerous?
- **Data Theft**: Credentials, financial info, and personal data can be stolen.
- **Malware Distribution**: Inject malicious payloads into downloads.
- **Corporate Risks**: Compromised employee devices can lead to network breaches.

---

## <a name="how-to-detect"></a>How to Detect an Evil Twin Attack
1. **Check for Duplicate SSIDs**: Use tools like `Kismet` or `NetStumbler`.
2. **Verify MAC Addresses**: Compare MAC addresses of networks with the same SSID.
3. **Monitor Signal Strength**: A sudden strong signal in a public place may be suspicious.
4. **Look for SSL Stripping**: Unexpected HTTP (not HTTPS) pages on secure sites.

---

## <a name="prevention"></a>Prevention Measures

### For Individuals
- 🔒 **Use a VPN**: Encrypt all traffic (e.g., NordVPN, ProtonVPN).
- 🚫 **Disable Auto-Connect**: Turn off "Connect Automatically" for Wi-Fi networks.
- 🌐 **Stick to HTTPS**: Use browser extensions like HTTPS Everywhere.
- 📱 **Avoid Public Wi-Fi**: Prefer mobile hotspots.

### For Organizations
- 🛡️ **Deploy WIPS**: Wireless Intrusion Prevention Systems (e.g., Cisco WIPS).
- 🔐 **Upgrade to WPA3**: Replace outdated WPA2 encryption.
- 📚 **Employee Training**: Teach staff to verify networks and use VPNs.

---

## <a name="examples"></a>Real-Life Examples
1. **2017 Starbucks Attack (Buenos Aires)**: Hackers created a fake "Starbucks" network to steal payment details.
2. **2024 Flight Wi-Fi Scam (Australia)**: Rogue network on a flight captured passenger credentials.

---

## <a name="tools"></a>Ethical Testing & Tools
**Disclaimer**: Only test on networks you own or have permission to audit.
- **Kali Linux**: Pre-installed tools like `aircrack-ng`, `reaver`.
- **Wi-Fi Pineapple**: Hardware for simulating attacks.
- **Fluxion**: Framework for creating captive portals.

```bash
# Example: Scan for nearby networks
sudo airmon-ng start wlan0
sudo airodump-ng wlan0mon
```
---
## Demo How It Works!..
![evil-twin-attack-explained-anim]()
<img src="https://github.com/user-attachments/assets/d3a642f5-12dc-40eb-96c7-f4aac40578d5" width="800" height="800" alt="Evil Twin Attack Banner">
