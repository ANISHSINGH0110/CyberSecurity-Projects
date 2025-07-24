# 🛡️ Cybersecurity Projects – Malware Analysis & Reverse Engineering

This repository showcases a collection of hands-on cybersecurity projects focused on **Malware Analysis**, **Reverse Engineering**, and **Threat Intelligence**. The goal is to develop the skills needed to analyze, understand, and document real-world malicious software using both **static and dynamic analysis techniques**.

---

## 📦 Project Overview

### 🔬 Malware and Reverse Engineering

Performing in-depth analysis of unknown executables using reverse engineering tools and techniques. Each project involves identifying file behavior, uncovering hidden payloads, detecting persistence mechanisms, and correlating IOCs (Indicators of Compromise).

#### Techniques Used:
- Static Analysis: Disassembling binaries, string extraction, header inspection
- Dynamic Analysis: Monitoring system behavior in a controlled environment
- Network Traffic Analysis: Observing outbound connections and C2 (Command & Control) patterns
- IOC Correlation: Identifying and documenting malicious artifacts

---

## 📁 Projects Included

### 1. 📄 **Static and Dynamic Analysis of Malware.Unknown.exe.malz**
- **Objective:** Analyze suspicious executable to detect host/network behaviors.
- **Tools Used:** FLOSS, Wireshark, Procmon, REMnux, FlareVM
- **Findings:**
  - Creates file `CR433101.dat.exe`
  - Uses `cmd.exe` with self-deletion and silent execution
  - Communicates with internal domain via HTTP (`favicon.ico`)
- **Outcome:** Identified host-level and network-level IOCs for malware detection.

---

### 2. 🐀 **Remote Access Trojan (RAT) – `RAT.Unknown.exe`**
- **Objective:** Perform **network-based analysis** of a suspected RAT.
- **Focus:** Capturing and analyzing communication patterns with the attacker’s server.
- **Tools:** Wireshark, INetSim, Fake DNS/HTTP servers
- **Key Observations:**
  - C2 traffic using non-standard ports
  - Beaconing to hardcoded IP addresses
  - Keep-alive and heartbeat packets
- **Result:** Extracted C2 IPs and behavioral signatures for defensive rules.

---

### 3. 🐚 **RAT Reverse Shell – `RAT.Unknown2.exe`**
- **Objective:** Analyze a reverse shell RAT that initiates outbound connections to an attacker's terminal.
- **Analysis Types:**
  - Static: Identified obfuscated strings and embedded IPs
  - Dynamic: Traced outbound TCP shell sessions on execution
- **Tools:** Procmon, Netcat, Wireshark, Ghidra
- **Outcome:** Reconstructed shell communication flow, mapped execution stages, and flagged the RAT’s persistence methods.

---

## 🔗 IOC Correlation

All projects include:
- IP addresses/domains contacted by malware
- Filenames and registry changes
- Self-deletion or persistence tactics
- Protocols and methods used for remote access or data exfiltration

These IOCs are cross-correlated using:
- Threat intel feeds (manual comparison)
- Pattern matching across binaries
- Timeline analysis

---

## 🧰 Tools & Technologies Used

| Category           | Tools / Frameworks                    |
|--------------------|----------------------------------------|
| Static Analysis     | FLOSS, Ghidra, PEiD                   |
| Dynamic Analysis    | FlareVM, Procmon, Wireshark, REMnux   |
| RAT Testing         | Netcat, INetSim, Fake DNS             |
| Analysis Environment| VirtualBox, Windows Sandbox           |

---

## 🎓 Learning Outcomes

- Hands-on experience in analyzing **realistic malware behavior**
- Developed a solid workflow for **reverse engineering and IOC extraction**
- Understood the working and detection of **remote access tools and reverse shells**
- Built a foundation in **threat hunting and malware triage**

---

## 👨‍💻 Author

**Anish Kumar Singh**  
Cybersecurity Enthusiast | Reverse Engineering Learner  
[GitHub](https://github.com/ANISHSINGH0110) | [LinkedIn](https://www.linkedin.com/in/anish-singh0110)

---

## ⚠️ Disclaimer

All analysis and malware execution were done in **isolated virtual environments** strictly for **educational and research purposes**. Do not attempt to run any malicious file on a production or personal system.



