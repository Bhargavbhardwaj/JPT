You can specify to use any or a group of these installed scripts; moreover, you can install other users’ scripts and use them for your scans. 

Let’s begin with the default scripts. You can choose to run the scripts in the default category using --script=default or simply adding -sC. 

In addition to default(opens in new tab), categories include auth, broadcast, brute, default, discovery, dos, exploit, external, fuzzer, 

&#x20;  intrusive, malware, safe, version, and vuln. A brief description is shown in the following table.







**Script Category     Description**



auth	         Runs authentication-related scripts

broadcast	     Discovers hosts by sending broadcast messages

brute	         Performs brute-force password auditing against logins



default          Runs default scripts (same as -sC)



discovery	     Retrieves accessible information, such as database tables and DNS names



dos	             Detects servers vulnerable to Denial of Service (DoS)



exploit	         Attempts to exploit various vulnerable services



external	     Checks using a third-party service, such as Geoplugin and Virustotal



fuzzer	         Launches fuzzing attacks



intrusive	     Runs intrusive scripts such as brute-force attacks and exploitation



malware	         Scans for backdoors



safe	         Runs safe scripts that won't crash the target

version	         Retrieves service versions

vuln	         Checks for vulnerabilities or exploits in a vulnerable service



Some scripts belong to more than one category. Moreover, some scripts launch brute-force attacks against services, 

while others launch DoS attacks and exploit systems. Hence, it is crucial to be careful when selecting scripts to run to avoid crashing services or exploiting them.



You can specify to use any or a group of these installed scripts; moreover, you can install other users’ scripts and use them for your scans. Let’s begin with the default scripts. You can choose to run the scripts in the default category using --script=default or simply adding -sC. In addition to default(opens in new tab), categories include auth, broadcast, brute, default, discovery, dos, exploit, external, fuzzer, intrusive, malware, safe, version, and vuln. A brief description is shown in the following table.



###### **### SAVING OUTPUTS**



Option	                                    Meaning

\-sV	                      Determine service/version info on open ports

\-sV --version-light	      Try the most likely probes (2)

\-sV --version-all	      Try all available probes (9)

\-O	                      Detect OS

\--traceroute	              Run traceroute to the target

\--script=SCRIPTS	      Nmap scripts to run

\-sC or --script=default      Run default scripts

\-A	                     Equivalent to -sV -O -sC --traceroute

\-oN	                     Save output in normal format

\-oG	                     Save output in a grepable format

\-oX	                     Save output in XML format

\-oA	                     Save output in normal, XML and Grepable formats





As the name implies, the **normal format** is similar to the output you get on the screen when scanning a target. You can save your scan in normal format by using -oN FILENAME; N stands for normal. In the AB, first enter the command **nmap -oN scan.nmap MACHINE\_IP**





The **grepable format** has its name from the command grep; grep stands for Global Regular Expression Printer. In simple terms, it makes filtering the scan output for specific keywords or terms efficient. You can save the scan result in a grepable format using **-oG FILENAME** .





The third format is **XML**. You can save the scan results in XML format using **-oX FILENAME**. The XML format would be most convenient for processing the output in other programs. Conveniently enough, you can save the scan output in all three formats using -oA FILENAME to combine **-oN, -oG, and -oX** for normal, grepable, and XML.





A fourth format is **script kiddie**. You can see that this format is useless if you want to search the output for any interesting keywords or keep the results for future reference. However, you can use it to save the output of the scan **nmap -sS 127.0.0.1 -oS FILENAME**, display the output filename, and look 31337 in front of friends who are not tech-savvy.

