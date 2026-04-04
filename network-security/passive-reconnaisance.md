📍 Module: Network Security
---------------------------

🧠 Room: Passive Reconnaissance
-------------------------------

🔍 Overview
-----------

Today I covered the basics of **Passive Reconnaissance**, the first room in the Network Security module on TryHackMe.

This module includes:

*   Passive Reconnaissance
    
*   Active Reconnaissance
    
*   Nmap Scanning Techniques
    
*   Protocols and Servers
    
*   Network Security Challenge
    

🛰️ What is Passive Reconnaissance?
-----------------------------------

Passive reconnaissance involves gathering information about a target **without directly interacting with it**, making it stealthy and undetectable.

✔️ No direct connection to the target✔️ Uses publicly available data✔️ Does not trigger alerts

⚔️ Passive vs Active Recon
--------------------------

Passive ReconActive ReconNo direct interactionDirect interaction with targetStealthyDetectableUses public dataSends requests to target

🛠️ Tools Learned
-----------------

### 🔹 whois

*   Used to query **WHOIS records**
    
*   Provides domain registration details
    

`   whois example.com   `

### 🔹 nslookup

*   Queries **DNS records**
    

`   nslookup example.com   `

### 🔹 dig

*   Advanced DNS query tool
    

`   dig example.com   `

🌐 Online Recon Tools
---------------------

### 🔹 DNSDumpster

*   Finds subdomains and DNS info
    

### 🔹 Shodan

*   Search engine for internet-connected devices
    
*   Useful for identifying exposed systems
    

📌 Key Takeaways
----------------

*   Passive recon is the **first step in penetration testing**
    
*   It helps gather intel without alerting the target
    
*   Tools like whois, nslookup, and dig are essential
    
*   Online tools enhance reconnaissance without direct interaction
    

⚠️ Pre-requisites
-----------------

*   Basic networking knowledge
    
*   Familiarity with command line
    
*   Recommended:
    
    *   Network Fundamentals
        
    *   Linux Fundamentals
        

📈 Progress
-----------

*   Passive Reconnaissance
    
*   Active Reconnaissance
    
*   Nmap Scanning
    

🚀 Notes
--------

This was a foundational room that sets the stage for deeper network scanning and enumeration techniques. Understanding passive recon is critical for staying stealthy during real-world assessments.