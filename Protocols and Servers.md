**Protocol**	**Default Port**	**Secured Protocol**	**Default Port with TLS**



HTTP	              80	      HTTPS	              443

FTP	              21	      FTPS	              990

SMTP	              25	      SMTPS	              465

POP3	              110	      POP3S	              995

IMAP	               143	      IMAPS	              993





###### **>>>>> Connecting via SSH**

On Linux, macOS, and Windows 10/11, you can connect to an SSH server using the command ***ssh username@10.48.160.251***. This command tries to connect to the server at the specified IP address with the given login name. If an SSH server is listening on the default port, it will ask you to provide the password for that user (or use your key if configured). Once authenticated, you have access to the target server's terminal.



###### **SSH Key Generation**



To set up key-based authentication, generate a key pair using ssh-keygen:



\# Generate an Ed25519 key (recommended for modern systems)

***ssh-keygen -t ed25519 -C "your\_email@example.com"***



\# For systems that don't support Ed25519, use RSA with 4096 bits

***ssh-keygen -t rsa -b 4096 -C "your\_email@example.com"***

Ed25519 keys are the current recommendation. They are shorter, faster, and considered more secure than RSA keys. RSA keys should use at least 4096 bits if Ed25519 is not available.



Your private key is stored in **\~/.ssh/id\_ed25519 (or \~/.ssh/id\_rsa)** and should be protected with a strong passphrase. The public key is stored with a .pub extension and can be safely shared.



***To enable key-based login on a server, add your public key to the \~/.ssh/authorized\_keys file on the remote system:***



\# Copy your public key to a remote server

***ssh-copy-id mark@10.48.160.251***



###### **>>>>> Useful SSH Options**



SSH has many useful features for penetration testers and system administrators:



\# Connect on a non-standard port

***ssh -p 2222 mark@10.48.160.251***



\# Use a specific private key

***ssh -i \~/.ssh/custom\_key mark@10.48.160.251***



\# Jump through a bastion/jump host to reach an internal server

***ssh -J bastion.example.com mark@internal-server***



\# Local port forwarding (access remote service through local port)

***ssh -L 8080:localhost:80 mark@10.48.160.251***



\# Dynamic port forwarding (SOCKS proxy)

***ssh -D 9050 mark@10.48.160.251***



\# Run a single command without interactive shell

***ssh mark@10.48.160.251 "cat /etc/passwd"***





###### **>>>>> Useful Tcpdump Filters**

###### 

When capturing traffic, effective filtering helps you focus on relevant packets:



\# Capture traffic on a specific port

***sudo tcpdump port 110 -A***



\# Capture traffic to/from a specific host

***sudo tcpdump host 10.20.30.148 -A***



\# Capture HTTP traffic (may include credentials in POST requests)

***sudo tcpdump port 80 -A***



\# Capture FTP traffic (credentials sent in cleartext)

***sudo tcpdump port 21 -A***



\# Write captured packets to a file for later analysis

***sudo tcpdump -w capture.pcap***



\# Read and analyse a capture file

***tcpdump -r capture.pcap -A***





###### **>>>>>Protocol and Port Reference**



The services covered in this room are listed in the following table, sorted by alphabetical order.



**Protocol	TCP Port	Application(s)	Data Security**

FTP	21	File Transfer	Cleartext

FTPS	990	File Transfer	Encrypted (implicit TLS)

HTTP	80	Worldwide Web	Cleartext

HTTPS	443	Worldwide Web	Encrypted (implicit TLS)

IMAP	143	Email (MDA)	Cleartext

IMAPS	993	Email (MDA)	Encrypted (implicit TLS)

POP3	110	Email (MDA)	Cleartext

POP3S	995	Email (MDA)	Encrypted (implicit TLS)

SFTP	22	File Transfer	Encrypted (SSH)

SMTP	25	Email (MTA)	Cleartext

SMTP Submission	587	Email (MTA, client submission)	STARTTLS\*

SMTPS	465	Email (MTA)	Encrypted (implicit TLS)

SSH	22	Remote Access and File Transfer	Encrypted

Telnet	23	Remote Access	Cleartext





###### **>>>>> Additional Tools to Explore**



Beyond Hydra, consider learning these tools that complement what this room covered:



**Tool	                                     Purpose**

Wireshark / tcpdump	        Network packet capture and analysis

Bettercap	               MITM attacks, ARP spoofing, and network reconnaissance

mitmproxy	              Interactive HTTPS proxy for inspecting and modifying traffic

testssl.sh	             Testing TLS/SSL configuration and vulnerabilities

Nmap	                    Port scanning, service detection, and scripting

CrackMapExec / NetExec	        Password spraying and lateral movement in Windows environments

Hashcat / John the Ripper	Offline password hash cracking

Burp Suite	              Web application security testing





###### **>>>> Defensive Checklist**



When assessing or securing systems, verify the following:



All services use TLS 1.2 or TLS 1.3 with strong cipher suites.

Cleartext protocols (Telnet, FTP, HTTP) are disabled or restricted to isolated networks.

SSH uses key-based authentication with password authentication disabled.

Strong password policies are enforced with breached password detection.

Account lockout or rate limiting is implemented for all authentication endpoints.

Multi-factor authentication is enabled for sensitive systems.

Network segmentation limits the impact of sniffing attacks.

Certificate validation is properly implemented to prevent MITM attacks.

HSTS (HTTP Strict Transport Security) is enabled for web applications to prevent SSL stripping.

Logging and monitoring detect authentication anomalies.

