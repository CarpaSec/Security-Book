# Web Enumeration

Web enumeration involves systematically extracting detailed information about a target web application, including its structure, functionality, and underlying technologies.&#x20;

Sitemaps: Provides a hierarchical diagram of the pages within a web application, useful for understanding the structure and navigation of the site.

* **Usage:** Many web applications include a sitemap (usually accessible as `/sitemap.xml`). Tools like web crawlers can also generate sitemaps.

[Testssl.sh](https://testssl.sh/) (CLI-based)**:** Tests TLS/SSL encryption strength and vulnerabilities in web servers.

```bash
./testssl.sh example.com
# General test of the SSL/TLS of a web server.
./testssl.sh --vulnerable example.com
# Checks for known vulnerabilities.
./testssl.sh --protocols example.com
# Tests supported protocols.
./testssl.sh --headers example.com
# Checks security headers.
`./testssl.sh --cipher-per-proto example.com`
# Lists ciphers per protocol for the target.
```

Nmap for Cipher Strength**:** Besides its primary function as a network scanner, Nmap can be used to test SSL/TLS cipher strength.

```bash
nmap --script ssl-cert,ssl-enum-ciphers -p 443 example.com
# Enumerates SSL/TLS ciphers and certificate details.
nmap --script ssl-known-key -p 443 example.com
# Checks for SSL keys known to be weak.
nmap --script ssl-date -p 443 example.com
# Compares the SSL certificate's date with the local system date.
nmap --script ssl-dh-params -p 443 example.com
# Shows Diffie-Hellman parameters.
nmap --script ssl-heartbleed -p 443 example.com
# Tests for the Heartbleed vulnerability.
```

Checking HTTP Headers**:** Analyzing HTTP response headers for security settings, server types, and other valuable information.

* **Usage:** Browser developer tools or command-line tools like `curl -I http://example.com` can be used to view headers.

Uniscan**:** A simple remote file, directory, and web structure enumerator.

Wmap**:** A web application vulnerability scanner, often used within the Metasploit Framework.

* **Note:** Integrated within Metasploit. Wmap is used to gather and store information about web applications and then identify vulnerabilities.
* Wmap is part of the [Metasploit Framework](https://www.metasploit.com/).

NmapAutomater (CLI-based)**:** A script that automates the scanning process with Nmap and other tools.

```bash
./nmapAutomator.sh example.com Quick
# Conducts a quick scan of the target.
./nmapAutomator.sh example.com Network
# Performs a detailed network scan.
./nmapAutomator.sh example.com Vuln
# Runs vulnerability scanning on the target.
./nmapAutomator.sh example.com Recon
# Gathers detailed reconnaissance information.
./nmapAutomator.sh example.com Full
# Executes a full range of scans (Quick, Network, and Vuln).
```

AutoRecon (CLI-based)**:** An automated reconnaissance tool that performs numerous scans and enumeration while being efficient.

```bash
autorecon example.com
# Performs a full reconnaissance scan on the target.
autorecon -vv example.com
# Runs the scan in very verbose mode.
autorecon -o /path/to/output example.com
# Specifies the output directory for scan results.
autorecon --single-target example.com
# Scans a single target.
autorecon --only-scans-dir example.com
# Only runs scans found in the "scans" directory.
```
