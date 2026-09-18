# footprinting-reconnaissance
Footprinting &amp; reconnaissance using multiple Kali Linux tools, plus network scanning with Zenmap.
## Overview
This project shows how I gathered public information about a target domain 
using several Kali Linux tools, as part of my cybersecurity traininh. I had written permission to test the training domain 
(networkwalks.com). I also scanned my own home network.

## Tools Used
| Tool | What it does |
|------|------|
| whois | Finds who owns a domain and when it was registered |
| whatweb | Finds what software/technology a website uses |
| nslookup | Finds the IP address behind a domain name |
| curl -I | Shows the website's response headers |
| wafw00f | Checks if a website has a firewall protecting it |
| dnsrecon | Finds all DNS records for a domain |
| Zenmap | Scans a local network to find connected devices |

## What I Found

**Domain Info (whois)**
- Domain: NETWORKWALKS.COM
- Registrar: GoDaddy
- Created: 6 Nov 2019
- Expires: 6 Nov 2027
- Name servers: NS6135.HOSTGATOR.COM, NS6136.HOSTGATOR.COM

**Website Technology (whatweb)**
- Runs WordPress 7.1
- Uses a plugin called WordPress Download Manager 3.3.58
- Server: Apache
- Site name: "Networkwalks Academy"
- Public email found: info@networkwalks.com

**IP Address (nslookup)**
- networkwalks.com → 192.232.216.135

**HTTP Headers (curl -I)**
- Uses HTTP/2
- WordPress API is publicly visible at /wp-json/
- Cookies are set securely (HttpOnly)

**Firewall Check (wafw00f)**
- Protected by ModSecurity (SpiderLabs) firewall

**DNS Records (dnsrecon)**
- Mail server: mail.networkwalks.com
- Hosted through GoDaddy/HostGator

**Home Network Scan (Zenmap)**
- Found 2 devices on my network:
  - 192.168.1.1 (my router)
  - 192.168.1.141 (my computer)

## What I Learned
This showed me how much public information is available about a website 
before anyone even tries to attack it. Gathering this information first is 
the foundation for every later step in cybersecurity testing.

## Disclaimer
This was done only with written permission for training purposes. 
No attacks or hacking were performed — only information gathering.
