Nmap, short for Network Mapper, is free, open-source software released under the GPL license, created by Gordon Lyon (Fyodor), a network security expert and open-source programmer. Nmap is an industry-standard tool for mapping networks, identifying live hosts, and discovering running services. Nmap’s scripting engine can further extend its functionality, from fingerprinting services to exploiting vulnerabilities. A Nmap scan usually goes through the steps shown in the figure below, although many are optional and depend on the command-line arguments you provide.

Learning Objectives
When we want to target a network, we want to find an efficient tool to help us handle repetitive tasks and answer the following questions:

Which systems are up?
What services are running on these systems?
The first question about finding live computers is answered in this room. This room is the first in a series of four Nmap rooms. The second question about discovering running services is answered in the next Nmap rooms, which focus on port scanning.

This room explains the steps Nmap takes to discover online systems before port scanning. This stage is crucial because attempting to port-scan offline systems will only waste time and generate unnecessary network noise.

We present the different approaches that Nmap uses to discover live hosts. In particular, we cover:

ARP scan: This scan uses ARP requests to discover live hosts
ICMP scan: This scan uses ICMP requests to identify live hosts
TCP/UDP ping scan: This scan sends packets to TCP ports and UDP ports to determine live hosts.
We also introduce two scanners, arp-scan and masscan, and explain how they overlap with part of Nmap’s host discovery.