Objective
Map TCP ports and identify exposed services on host 10.80.138.85 (TryHackMe) using Nmap, as part of an initial reconnaissance study.

Commands Used

Full TCP port scan:
nmap -sS -p- -T4 -oN scan_full.txt 10.80.138.85

Service identification on specific ports:
nmap -sV -p22,80,443 -oN scan_specific.txt 10.80.138.85

Findings
Multiple TCP ports were identified as open, indicating an extensive attack surface. The following ports were observed:
21 (FTP), 53 (DNS), 80 (HTTP), 135 (RPC), 3389 (RDP), 5985 (WinRM), 49666 and 49669 (dynamic ports).

Interpretation
The exposure of administrative services such as RDP (3389) and WinRM (5985) may represent a high risk if not properly secured.
High, unidentified ports may be associated with internal services or dynamic RPC ports, increasing the attack surface and requiring further investigation.

Detection (SOC Perspective)
A SOC could detect this activity through port scan alerts by observing multiple SYN packets sent to different ports within a short time frame.
IDS/IPS tools or firewalls could generate alerts for horizontal scanning behavior originating from a single IP address.
