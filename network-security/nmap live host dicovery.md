`# 🌐 Nmap Live Host Discovery - TryHackMe Notes## 

📌 Overview**Nmap (Network Mapper)** is a powerful open-source tool created by **Gordon Lyon (Fyodor)** for network discovery and security auditing.

This room focuses on **identifying live hosts** before performing port scans.---## 🎯 Learning ObjectiveAnswer the key question:- **Which systems are up (alive)?**> ⚠️ Scanning offline hosts wastes time and creates unnecessary network noise.---## 

🔍 Host Discovery Methods### 1. 🧾 ARP Scan- Uses **ARP requests** to find live hosts on a local network- Fast and reliable within LAN
                             ## 2\. 📡 ICMP Scan

*   Uses ICMP echo requests (ping)
    

`nmap -PE` 

*   Checks if a host responds to ping
    

### 3\. 🔌 TCP/UDP Ping Scan

*   Sends packets to specific ports
    

`   nmap -PS     # TCP SYNnmap -PU     # UDP   `

*   Useful when ICMP is blocked
    

⚙️ Additional Tools
-------------------

### 🛠️ arp-scan

*   Dedicated ARP-based host discovery tool
    
*   Works on local networks
    

### ⚡ masscan

*   Extremely fast scanner
    
*   Used for large-scale network scanning
    

🔑 Key Takeaways
----------------

*   Host discovery is the **first step** before port scanning
    
*   Nmap provides multiple techniques depending on network conditions
    
*   Different methods help bypass firewall restrictions
    
*   Tools like **arp-scan** and **masscan** complement Nmap
    

🚀 Summary
----------

*   Identify **live systems efficiently**
    
*   Avoid unnecessary scans
    
*   Prepare for deeper analysis (port scanning)