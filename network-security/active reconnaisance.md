# 🔍 Active Reconnaissance - TryHackMe Notes## 

📌 Overview:

In this room, we move from **Passive Reconnaissance** to **Active Reconnaissance**.- **Passive Reconnaissance**: Gathering information without interacting with the target.- **Active Reconnaissance**: Directly interacting with the target system.> 

⚠️ Important: Active reconnaissance requires **legal authorization**, as it involves direct contact with the target and can leave logs.---## ⚡ What is Active Reconnaissance?Active reconnaissance involves:- Making **direct connections** to target systems- Interacting with services (web servers, ports, etc.)- Collecting information that may be logged by the target### 

🧠 Key InsightEvery interaction can leave traces such as:- IP address- Timestamp- Duration of connectionHowever, some actions (like browsing a website) may appear as **normal user activity**, which can help avoid detection.---## 🛠️ Tools Covered### 1. 🌐 Web Browser + Developer Tools- Inspect network traffic- Analyze requests/responses- View source code- Identify APIs and endpoints> Browsers can be "armed" into powerful reconnaissance tools.---### 2. 📡 Ping**Purpose**: Check if a host is reachable```bashping` 

**What it reveals:**

*   Host availability
    
*   Round-trip time (latency)
    

### 3\. 🧭 Traceroute

**Purpose**: Trace the path packets take to reach the target

`   traceroute    # Linuxtracert       # Windows   `

**What it reveals:**

*   Network path (routers/hops)
    
*   Network delays
    
*   Infrastructure layout
    

### 4\. 🔌 Telnet

**Purpose**: Connect to a remote service on a specific port

`telnet`  

**What it reveals:**

*   Open ports
    
*   Service behavior
    
*   Banner information (sometimes)
    

### 5\. 🧰 Netcat (nc)

**Purpose**: Versatile networking tool for communication and testing

`nc`  

**Capabilities:**

*   Port scanning
    
*   Banner grabbing
    
*   File transfer
    
*   Reverse shells (advanced use)
    

🔬 Practical Labs
-----------------

In this room, hands-on labs help reinforce:

*   Using tools in real scenarios
    
*   Observing system responses
    
*   Understanding network behavior
    

🔐 Key Takeaways
----------------

*   Active reconnaissance involves **direct engagement** with the target.
    
*   It is **detectable** and leaves logs.
    
*   Always ensure **legal permission** before performing it.
    
*   Simple tools can provide **valuable insights** into systems and networks.
    
*   Blending in with normal traffic (e.g., web browsing) can reduce suspicion.
    

🚀 Learning Outcome
-------------------

After completing this room, you should be able to:

*   Understand the difference between passive and active recon
    
*   Use basic networking tools effectively
    
*   Analyze network paths and services
    
*   Perform reconnaissance responsibly and legally