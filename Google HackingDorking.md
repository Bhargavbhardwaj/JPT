###### **Google Hacking / Dorking**

Google's advanced search operators let you filter results in ways that can surface sensitive content indexed from your target. By combining operators, you can find exposed admin panels, leaked documents, and login pages that the site owner never intended to be public.



###### Filter	           Example	                       Description

site	         site:tryhackme.com	           Returns results only from the specified domain

inurl	         inurl:admin	                   Returns results with the specified word in the URL

filetype	 filetype:pdf	                   Returns results of a specific file type

intitle	         intitle:admin	                   Returns results with the specified word in the page title

intext	         intext:password	           Returns results containing the specified word in the body

cache	         cache:tryhackme.com	           Shows Google's cached version of the page





For example, ***site:tryhackme.com filetype:pdf*** would return all PDFs indexed from tryhackme.com. You can combine multiple filters in a single query. More information is available at Wikipedia: Google Hacking(opens in new tab).



###### **Wappalyzer**

Wappalyzer(opens in new tab) is a browser extension and online tool that identifies the technologies a website uses, frameworks, CMS platforms, CDNs, analytics tools, payment processors, and more. It can often detect version numbers, which helps when searching for known vulnerabilities. Install it from your browser's extension store and visit any site to see the tech stack immediately.





###### **Wayback Machine**

The Wayback Machine is an archive of the Internet dating back to the late 1990s. Search for a domain, and you'll see every snapshot captured over time. This is useful for finding pages that have been removed from the live site but may still be accessible: old login forms, forgotten API endpoints, or content that was published briefly before being taken down.





###### **Gobuster**

Gobuster is an open-source enumeration tool written in Go. It supports multiple modes: ***directory/file enumeration (dir)***, DNS subdomain enumeration (dns), and virtual host enumeration (vhost). It's pre-installed on the AttackBox and included by default in Kali Linux.



Run gobuster --help to see the available commands and global flags:

&#x20;  

**Flag	                                Description**

\-t / --threads	             Number of concurrent threads (default: 10). Increase for faster scans.

\-w / --wordlist	             Path to the wordlist file. Required for all modes.

\-o / --output	             Write results to a file instead of stdout.

\--delay	                     Wait time between requests: useful against rate-limited servers.

