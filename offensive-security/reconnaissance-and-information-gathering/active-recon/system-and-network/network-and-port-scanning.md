# Network & Port Scanning

Port Scanning and Service Identification in active reconnaissance are crucial for discovering open ports on a target system and identifying the services running on those ports. This information helps in understanding the network's architecture, the types of applications and services in use, and potential vulnerabilities. Port scanners send packets to specific ports on a network and listen for responses, while service identification tools analyze these responses to determine what services are active.

[**Nmap** ](https://nmap.org/)**(CLI-based):** Identifies open ports, running services, and OS versions.

```bash
nmap -p 1-65535 192.168.1.1
# Scans all ports on a host.
nmap -sV 192.168.1.1
# Detects service versions.
nmap -O 192.168.1.1
# Detects the operating system.
nmap --script http-headers 192.168.1.1
# Fetches HTTP headers.
nmap -sU 192.168.1.1
# UDP scanning.
```

[**Masscan** ](https://github.com/robertdavidgraham/masscan)**(CLI-based)** Extremely fast port scanner, useful for scanning large networks.

```bash
masscan -p80,443 10.0.0.0/8
# Scans for ports 80 and 443 over a large IP range.
masscan --rate 10000 -p0-65535 192.168.1.1
# Scans all ports at a high rate.
masscan --top-ports 100 192.168.1.0/24
# Scans top 100 ports on a subnet.
```

**Netcat (CLI-based):** Versatile networking tool, often used for port scanning and banner grabbing.

```bash
nc -zv 192.168.1.1 20-30
# Scans a range of ports on a host.
nc -lvp 4444
# Listens on a specific port.
nc 192.168.1.1 3389
# Connects to a specific port.
```

#### [Advanced IP Scanner](https://www.advanced-ip-scanner.com/): Fast, robust, and easy-to-use IP scanner for Windows.

[**Angry IP Scanner**](https://angryip.org/)**:** Fast and user-friendly network scanner for Windows, Linux, and Mac.

**Zenmap:** Official Nmap GUI, making scan results easier to read and interpret.

[**Wireshark**](https://www.wireshark.org/)**:** Network protocol analyzer that can capture and display network traffic in real-time.

**Nessus:** Vulnerability scanner that can also perform port scanning and service identification.

[**OpenVAS**](https://www.openvas.org/)**:** Open-source vulnerability assessment tool that includes port scanning functionality.

[**Fing**](https://www.fing.com/)**:** Network discovery and scanning tool with a focus on simplicity and ease of use.

[**TCPdump** ](http://www.tcpdump.org/)**(CLI-based):** Powerful command-line packet analyzer for network traffic monitoring.

```bash
tcpdump -i eth0
# Captures on the eth0 interface.
tpdump -c 100
# Captures 100 packets then stops.
tcpdump -w capture.pcap
# Writes captured packets to a file.
tcpdump port 80
# Captures packets on port 80.
```

**SolarWinds Port Scanner:** Free tool that delivers fast and accurate identification of open, closed, and filtered ports.

[**Metasploit**](https://www.metasploit.com/)**:** Advanced open-source framework for developing, testing, and executing exploits.

[hping ](http://www.hping.org/)**(CLI-based):** Command-line oriented TCP/IP packet assembler/analyzer, used for port scanning.

```bash
hping3 -S -p 80 192.168.1.1
# SYN scan on port 80.
hping3 --scan 1-30 -S 192.168.1.1
# Scans ports 1-30 using SYN packets.
hping3 -F -p 139 192.168.1.1
# FIN scan on port 139.
```

**Unicornscan (CLI-based):** Attempts to improve the efficiency and flexibility of network scanning.

```bash
unicornscan 192.168.1.1:a
# Scans all ports.
unicornscan -mU 192.168.1.1
# UDP scan.
unicornscan -I 192.168.1.1
# Scans for active hosts.
```

**Scanrand (CLI-based):** Extremely fast port, network, and enumeration tool. Scanrand commands offer high-speed scanning and are often combined with other analysis tools.

**SuperScan:** Windows-only port scanning tool, ping sweep, and resolver.

**P0f:** Passive OS fingerprinting tool, used to identify the operating system of the target.

**Network Miner:** Network Forensic Analysis Tool (NFAT) for Windows that can detect the OS, hostname, and open ports of network hosts through packet sniffing.

**NetDiscover (CLI-based):** An active/passive address reconnaissance tool, primarily for those networks without DHCP.

```bash
netdiscover -r 192.168.1.0/24
# Scans the given range.
netdiscover -i eth0
# Scans on the eth0 interface.
netdiscover -p
# Passive mode
```
