Objective
The objective of this activity was to practice basic and advanced Nmap scanning techniques, comparing a simple SYN scan with a more comprehensive full-port and service detection scan.

Commands Used
Initial Scan (Basic SYN Scan):
nmap -sS 10.80.156.206
Comprehensive Scan (Full Port + Service Enumeration):
nmap -sS -sV -p- -T4 -oN scan_full.txt 10.80.156.206

Key Findings
The initial SYN scan identified multiple open TCP ports on the target host.
However, this scan provided limited information regarding the services and versions running on those ports.

The comprehensive scan significantly expanded the visibility of the target by:
Enumerating all 65,535 TCP ports
Identifying service versions
Providing deeper insight into exposed services
This additional information is critical for vulnerability assessment, as version detection enables correlation with known CVEs and misconfigurations.
Security Operations (SOC) Perspective

From a defensive standpoint, aggressive scans such as:
nmap -A -p- -T5 IP

are likely to trigger detection mechanisms due to:

High packet rate
Full port enumeration
Service and OS detection probes
Script execution (NSE)
Such activity may be classified as reconnaissance or potential intrusion attempt.

In contrast, slower and less intrusive scans such as:

nmap -sS -T2 IP
generate reduced network noise and lower traffic intensity, potentially decreasing the likelihood of immediate detection. However, even low-and-slow scanning may still be identified by advanced monitoring systems that analyze behavioral patterns over time.
