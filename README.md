# 🕵️ Wireshark Lab for Network Security & Forensics

## 📌 Overview
This lab demonstrates how to use **Wireshark** to capture, analyze, and investigate network traffic in a controlled environment.  
It simulates common cyberattacks (port scans, brute force, ICMP floods, DNS tunneling, etc.) and shows how to detect them at the packet level.  
The goal is to build practical **SOC analyst skills** in network forensics.

---

## ⚙️ Lab Setup
- **Platform**: VMware Workstation / Player
- **VMs**:
  - Windows VM (Wireshark installed)
  - Linux VM (attack simulation)
- **Network**: NAT or Host-Only network so VMs can communicate
- **Tools**:
  - Wireshark (packet capture)
  - nmap (port scanning)
  - hydra (brute force)
  - curl / ping (traffic generation)
  - iodine (DNS tunneling)
  - EICAR test file (safe malware simulation)

---

## 🧪 Attack Simulations
1. **Port Scanning**
   ```bash
   nmap -p 1-1000 <target_IP>
2. **Brute Force Attack**
   ```bash
   hydra -l testuser -P /usr/share/wordlists/rockyou.txt ssh://<target_IP>
3. **Ping Flood (ICMP Flood)**
   ```bash
   ping <target_IP> -f
4. **HTTP POST with Credentials**
   ```bash
   curl http://<target_IP> --data "username=admin&password=1234"


   
