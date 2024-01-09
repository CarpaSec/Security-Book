# Service Enumeration

### SMB Scanning Tools

**Smbclient:**&#x20;

```bash
smbclient -L //TARGET_IP 
# Lists SMB shares on the target.
smbclient //TARGET_IP/share 
# Connects to a specific SMB share.
smbclient -U username //TARGET_IP/share 
# Connects with a specific username.
smbclient //TARGET_IP/share -I TARGET_IP 
# Connects when NetBIOS names won’t resolve.
smbclient //TARGET_IP/share -c 'ls' 
# Lists contents of a share.
smbclient -N -L //TARGET_IP:
# Lists SMB shares on the target without asking for a password (-N flag).
smbclient //TARGET_IP/IPC$ -U username%password:
# Connects to the IPC$ share with specified username and password.
smbclient //TARGET_IP/share -c 'recurse; ls':
# Recursively lists the contents of a share.
smbclient //TARGET_IP/share -Tc backup.tar:
# Creates a tarball of the share's contents.
smbclient -g -L //TARGET_IP:
# Lists shares in a grep-able format.
```

**Enum4linux:**&#x20;

```bash
enum4linux -a TARGET_IP 
# Performs all basic enumeration of Windows or Samba systems.
```

**CrackMapExec:**

```bash
 crackmapexec smb TARGET_IP 
 # Performs various SMB operations.
```

**Nmap SMB Scripts:**

```bash
nmap --script smb-enum-shares.nse -p445 TARGET_IP 
# Enumerates SMB shares.
nmap --script smb-os-discovery.nse -p445 TARGET_IP 
# Discovers the OS of the target.
```

**Responder:**

```bash
responder -I eth0 
# Listens for SMB/LMNR/NBT-NS/HTTP/MDNS/FTP/DNS queries.
```

### SNMP Scanning Tools

[**Snmpwalk**](http://www.net-snmp.org/)**:**

```bash
snmpwalk -v1 -c public TARGET_IP 
# Walks SNMP MIBs using v1 and public community string.
snmpwalk -v2c -c public TARGET_IP 
# Uses version 2c.
snmpwalk -v2c -c public -O e TARGET_IP:
# Walks the SNMP tree with v2c, public community string, and enumerates OIDs.
snmpwalk -v3 -l authPriv -u user -A pass -X privpass TARGET_IP:
# Uses SNMPv3 with authentication and privacy passwords.
snmpwalk -v1 -c public -O n TARGET_IP:
# Walks SNMP MIBs using v1 and displays results numerically.
snmpwalk -v2c -c public -Cp TARGET_IP:
# Walks with v2c and prints the statistics of the operation.
snmpwalk -v1 -c public -Cf TARGET_IP:
# Walks with v1 and fast mode (no retries).
```

**Snmp-check:**

```bash
snmp-check TARGET_IP 
# Enumerates SNMP device information.
```

**Nmap SNMP Scripts:**

```bash
nmap -sU -p 161 --script=snmp-hh3c-logins TARGET_IP 
# Checks for HP devices.
nmap -sU -p 161 --script=snmp-win32-users TARGET_IP 
# Enumerates Windows users.
```

**Snmpenum:**

```bash
snmpenum TARGET_IP public windows.txt 
# Enumerates Windows SNMP info.
```

**Onesixtyone:**

```bash
onesixtyone -c community -i hosts.txt 
# SNMP scanner for specified hosts.
```

### DNS Scanning Tools

**Dnsenum:**

```bash
dnsenum example.com 
# Enumerates DNS information of a domain.
```

**Dnsrecon:**

```bash
dnsrecon -d example.com 
# Basic DNS enumeration.
dnsrecon -d example.com -t axfr 
# Attempts DNS zone transfer.
dnsenum --noreverse example.com:
# Enumerates DNS information without performing reverse lookups on ranges.
dnsenum --subfile subdomains.txt example.com:
# Uses a custom file for subdomain brute-forcing.
dnsenum --enum example.com:
# Performs standard enumeration plus additional DNS queries.
dnsenum --google example.com:
# Uses Google to enumerate subdomains.
dnsenum --privns only example.com:
# Enumerates only private nameservers.
```

**Fierce:**

```bash
 fierce --domain example.com 
 # Scans and identifies IPs and hosts.
```

**Nmap DNS Scripts:**

```bash
nmap --script dns-brute.nse example.com 
# Performs DNS subdomain brute-forcing.
```

**Host:**

```bash
host -t ns example.com 
# Finds the name servers for a domain.
host -t mx example.com 
# Retrieves the mail servers for a domain.
```

### SMTP Service Scanning

**Smtp-user-enum:** Enumerates users on an SMTP server by querying the SMTP service.

```bash
smtp-user-enum -M VRFY -U users.txt -t TARGET_IP 
# enumerate users.
```

**Swaks:** SMTP transaction tester, useful for testing SMTP server configurations.

```bash
swaks --to user@example.com --server TARGET_IP 
# test SMTP.
```

### Database Service Scanning

**Sqlmap:**

```bash
sqlmap -u "http://TARGET_IP/page?id=1"
# Tests for SQL injection at the given URL.
sqlmap -u "http://TARGET_IP/page" --data="id=1"
# POST request testing for SQL injection.
```

**Nmap Scripts for Databases:**

```bash
nmap -p 3306 --script=mysql-enum TARGET_IP
# MySQL service enumeration.
nmap -p 1433 --script=ms-sql-info TARGET_IP
# Microsoft SQL Server information enumeration.
```

### LDAP Service Scanning

**Nmap LDAP Scripts:**

```bash
nmap -p 389 --script=ldap-search TARGET_IP
# Performs an LDAP search.
nmap --script ldap-brute --script-args ldap.base='"dc=example,dc=com"' TARGET_IP
# Brute-force against LDAP.
```

**Ldapsearch:**

<pre class="language-bash"><code class="lang-bash">ldapsearch -x -b "dc=example,dc=com" -H ldap://TARGET_IP
# Searches the LDAP directory.
<strong>ldapsearch -x -h TARGET_IP -b "dc=example,dc=com"
</strong><strong># Basic LDAP search.
</strong>ldapsearch -x -LLL -H ldap://TARGET_IP -b "dc=example,dc=com" "(objectClass=*)"
# Fetches all objects.
ldapsearch -x -D "cn=admin,dc=example,dc=com" -w secret -b "dc=example,dc=com"
# Binds as a user.
ldapsearch -x -H ldap://TARGET_IP -b "dc=example,dc=com" "(uid=username)"
# Searches for a specific UID.
ldapsearch -x -H ldap://TARGET_IP -ZZ -b "dc=example,dc=com"
# Performs a search with StartTLS.
</code></pre>

### Kerberos Service Scanning

**Kerbrute:**

```bash
kerbrute userenum --dc TARGET_IP -d example.com userlist.txt
# Enumerate valid usernames.
```

**Nmap Kerberos Scripts:**

```bash
nmap --script=krb5-enum-users --script-args krb5-enum-users.realm='DOMAIN',userdb=users.txt TARGET_IP
# Enumerates Kerberos users.
```
