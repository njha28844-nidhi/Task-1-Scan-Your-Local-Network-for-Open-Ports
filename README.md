# Task-1-Scan-Your-Local-Network-for-Open-Ports
Nmap subnet scan &amp; analysis for 192.168.29.0/24 — outputs, screenshots, PCAPs, and findings (authorized lab)
# Task 1 — Network Discovery & Port Scanning (192.168.29.0/24)

**Date:** 2025-11-13  
**Scope:** `192.168.29.0/24` (authorized lab network)  
**Tools used:** `nmap`, `tcpdump`/`wireshark` (optional), `grep`, editor for notes

---

## Summary
This repository documents a structured network discovery and port-scanning exercise performed against an authorized lab subnet. The goal was to identify live hosts, enumerate open ports and services, and provide a brief analysis of potential security implications and next steps for further testing.

---

## Methodology (high level)
1. **Host discovery** — Identify live hosts in the subnet.  
2. **Port enumeration (top/common ports)** — Quickly identify commonly-open ports per host.  
3. **Full-port TCP SYN scan** — Scan all TCP ports on discovered hosts to find all listening services.  
4. **Service research** — For each discovered service, note the typical application, known risks, and relevant exploitation paths or hardening recommendations.  
5. **Evidence collection** — Save Nmap outputs, screenshots, and optional pcap captures.  
6. **Document findings** — Summarize hosts, ports, and suggested mitigations.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


### 1. Host discovery (ping scan)
 
sudo nmap -sS 192.168.29.0/24 

sudo nmap -sS -P- 192.168.29.0/24 
