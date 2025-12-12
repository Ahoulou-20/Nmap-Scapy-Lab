# Network Security Analysis: From Reconnaissance to Intrusion Detection

A comprehensive hands-on laboratory exploring essential network security tools for reconnaissance, enumeration, and traffic analysis.

## 🎯 Objectives

- Perform network reconnaissance and host discovery using Nmap
- Enumerate services and detect vulnerabilities
- Craft and analyze network packets with Scapy
- Inspect and filter network traffic using Wireshark
- Understand the attacker's perspective in penetration testing

## 🛠️ Tools Used

- **Nmap** - Network scanner for host discovery and service enumeration
- **Scapy** - Python-based packet manipulation and analysis tool
- **Wireshark** - Network protocol analyzer for traffic inspection

## 🔬 Lab Environment
```
Attacker Machine:  Kali Linux (192.168.121.128)
Target Machine:    Windows 10 (192.168.121.133)
Network Range:     192.168.121.0/24
```

## 📋 Exercises Performed

### 1. Nmap Reconnaissance

#### Host Discovery (Ping Sweep)
```bash
nmap -sn 192.168.121.0/24
```
Identified live hosts on the network.

#### OS Detection
```bash
sudo nmap -O 192.168.121.133
```
Determined target operating system through TCP/IP fingerprinting.

#### Service & Version Detection
```bash
nmap -p21 -sV -A -T4 192.168.121.133
```
Enumerated services and detected versions for vulnerability assessment.

#### SMB Enumeration
```bash
nmap --script smb-enum-shares.nse -p445 192.168.121.133
smbclient //192.168.121.133/print$ -N
```
Tested for SMB misconfigurations and anonymous access.

### 2. Scapy Packet Analysis

#### Traffic Sniffing
```python
# Capture all traffic
sniff()

# Capture on specific interface
sniff(iface="eth1")

# Filter ICMP packets
sniff(iface="eth1", filter="icmp", count=5)
```

#### Packet Storage and Analysis
```python
captured_packets = sniff(iface="eth1", filter="icmp", count=5)
captured_packets.summary()
```

### 3. Wireshark Traffic Inspection

- Live packet capture on network interface
- Protocol-level analysis (TCP/IP stack)
- Real-time traffic filtering and inspection

## 🔑 Key Findings

- Successfully identified active hosts and open ports
- Detected service versions useful for vulnerability research
- Captured and analyzed ICMP, DNS, and ARP traffic
- Demonstrated SMB enumeration techniques
- Understood packet structure at different OSI layers

## 📚 Skills Demonstrated

✅ Network reconnaissance and mapping  
✅ Service enumeration and fingerprinting  
✅ Packet crafting and manipulation  
✅ Traffic analysis and filtering  
✅ Security assessment methodology  

## 🎓 Learning Outcomes

This lab provided practical experience with:
- The reconnaissance phase of penetration testing
- How attackers map networks and identify vulnerabilities
- Defensive traffic monitoring and analysis techniques
- Understanding network protocols at a deeper level

## ⚠️ Ethical Notice

All activities were performed in a controlled lab environment with proper authorization. These tools should only be used for legitimate security testing, research, or educational purposes.

## 📖 Documentation

Full lab report with detailed screenshots available in `Lab_Documentation.pdf`

## 🔗 Connect

Feel free to reach out for discussions on network security and ethical hacking!

---

**Repository Structure:**
```
├── README.md
├── Lab_Documentation.pdf
├── screenshots/
│   ├── nmap_scans/
│   ├── scapy_analysis/
│   └── wireshark_captures/
└── scripts/
    └── scapy_examples.py
```
```

---

# 📱 LinkedIn Post

## Option 1 - Professional & Educational
```
🔐 Network Security Analysis: Hands-On Lab Completed

Just finished an intensive lab exploring three essential cybersecurity tools: Nmap, Scapy, and Wireshark.

🎯 What I practiced:
- Network reconnaissance and host discovery
- Service enumeration and OS fingerprinting
- SMB vulnerability assessment
- Packet crafting and traffic analysis
- Real-time protocol inspection

💡 Key Takeaway:
Understanding how attackers map networks during reconnaissance is crucial for building better defenses. These tools serve dual purposes—offensive testing and defensive monitoring.

🚀 The Challenge:
Filtering and interpreting massive amounts of network traffic requires patience and a solid understanding of protocols. Scapy's flexibility is powerful but demands precision in packet manipulation.

📌 Why This Matters:
In real-world penetration tests, reconnaissance is the foundation. The information gathered here guides every subsequent attack vector. For defenders, these same tools help detect anomalies and potential intrusions.

Full lab documentation available on my GitHub! 

#Cybersecurity #EthicalHacking #NetworkSecurity #Nmap #Wireshark #Scapy #PenetrationTesting #InfoSec
```

---

## Option 2 - Concise & Technical
```
🛡️ Completed: Network Security Analysis Lab

Explored the reconnaissance-to-detection pipeline using:
→ Nmap for host/service discovery
→ Scapy for packet manipulation
→ Wireshark for traffic analysis

Most Challenging: Crafting precise Scapy filters to isolate specific protocols in high-traffic environments.

Real-World Impact: These tools form the backbone of penetration testing and network defense. Understanding packet-level behavior is essential for both red and blue teams.

Lab docs & code on GitHub 👨‍💻

#NetworkSecurity #Cybersecurity #EthicalHacking #Nmap #Wireshark #Scapy
```

---

## Option 3 - Story-Driven
```
🔍 From Reconnaissance to Intrusion Detection: My Latest Lab

Ever wondered how hackers map your network before an attack? I just completed a hands-on lab that walks through exactly that process.

Using Kali Linux, I:
✓ Discovered live hosts (Nmap ping sweeps)
✓ Fingerprinted OS and services
✓ Tested for SMB misconfigurations
✓ Crafted custom packets (Scapy)
✓ Analyzed traffic at the protocol level (Wireshark)

🎯 The Reality Check:
What took me several commands could be automated by attackers in seconds. Defense requires understanding offense.

📊 Biggest Learning:
Network security isn't just about firewalls—it's about understanding every packet, every protocol, every potential entry point.

Documentation available on GitHub. Always learning, always securing.

#CyberSecurity #NetworkSecurity #EthicalHacking #PenetrationTesting #InfoSec #TechLearning
