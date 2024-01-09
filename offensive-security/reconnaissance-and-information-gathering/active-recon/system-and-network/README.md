# System & Network

Network Scanning and Enumeration involve actively probing a network or system to identify active hosts, open ports, services, and vulnerabilities. This type of reconnaissance is essential in the initial phase of penetration testing and cybersecurity assessments.

## Explanation and Methodologies

**Host Discovery:** Identifying live hosts in the network. Techniques include ping sweeps and ARP scanning.

**Port Scanning:** Determining open ports on discovered hosts. Techniques vary from a simple TCP connect scan to more sophisticated SYN stealth scans.

**Service Enumeration:** Identifying services running on open ports and gathering information like service type, version, etc.

**OS Fingerprinting:** Determining the operating systems of the hosts.

**Vulnerability Scanning:** Identifying potential vulnerabilities in the hosts, services, or applications.

**Network Mapping:** Visualizing the network layout, understanding the topology and interconnections between hosts.

## Network Scanning and Enumeration

[**Nmap**](https://nmap.org/) **(CLI-based):** Scans for open ports, identifies services and operating systems.

```bash
nmap -sS 192.168.1.1 
# Stealth SYN scan for open ports.
nmap -sV -p 22,80 192.168.1.1
# Service version detection on specific ports.
nmap -O 192.168.1.1
# OS detection.
nmap -sC 192.168.1.1
# Scan with default Nmap scripts.
nmap --script vuln 192.168.1.1
# Vulnerability scanning with Nmap scripts.
nmap -6 IPv6Address
# IPv6 scanning.
nmap -p 1-65535 192.168.1.1
# Full range port scan.
```

[**Wireshark**](https://www.wireshark.org/)**:** Network protocol analyzer for network troubleshooting and analysis.

<details>

<summary>Wireshark</summary>

[Wireshark User's Guide](https://www.wireshark.org/docs/wsug\_html\_chunked/)

[Wireshark Master Class](https://www.youtube.com/watch?v=OU-A2EmVrKQ\&list=PLW8bTPfXNGdC5Co0VnBK1yVzAwSSphzpJ) - Great YouTube playlist

</details>

**Netcat (CLI-based):** Networking utility for reading/writing network connections.

```bash
nc -zv 192.168.1.1 20-30
# Port scanning.
nc -lvp 4444
# Set up a listener on a specific port for incoming connections.
nc 192.168.1.1 3389
# Connect to a specific port on a host.
echo "GET / HTTP/1.1" | nc 192.168.1.1 80
# Send HTTP requests.
nc -u 192.168.1.1 53
# UDP mode.
```

**Masscan (CLI-based):** Ultra-fast port scanner, scanning large networks.

```bash
masscan -p80,443 10.0.0.0/8
# Scans large network for specific ports.
masscan --rate 10000 -p0-65535 192.168.1.1
# Scans all ports at a high rate.
masscan --top-ports 100 192.168.1.0/24
# Scans top 100 ports.
masscan -pU:53,111,137 --banners 192.168.1.0/24
# UDP scan with banner grabbing.
```

[**Angry IP Scanner**](https://angryip.org/)**:** Fast IP and port scanner with a GUI.
