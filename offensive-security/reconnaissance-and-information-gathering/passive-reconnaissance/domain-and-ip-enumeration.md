# Domain & IP Enumeration

## Domains

A domain, in the context of networking and cybersecurity, is an area of the internet that's controlled by a specific entity or organization. It's most commonly understood as the part of a website's URL that identifies it uniquely on the web. For instance, in the URL "[www.example.com](http://www.example.com)," "example.com" is the domain. Domains are organized in a hierarchical structure with top-level domains (TLDs) like ".com", ".org", ".net", etc., at the top, followed by second-level domains (like "example" in "example.com"), and potentially further subdivisions.

Domains are essential for the functioning of the internet, providing human-readable addresses for websites and services. They play a crucial role in cybersecurity, as understanding and managing the domain landscape of an organization is key to securing its digital presence and assets.

## DNS and Domain Information&#x20;

**Whois Lookup** - Retrieves crucial registration details about a domain, including the owner's contact info, registration date, and registrar.

```bash
# Fetch registration details for example.com
whois example.com
```

[**Robtex** ](https://www.robtex.com/)- Provides DNS and network information, including shared hosting and reverse DNS.

[**MXToolbox**](https://mxtoolbox.com/) - Offers a suite of network diagnostic tools, including DNS checks, MX record lookups, and blacklist checks.

[**ViewDNS.info**](https://viewdns.info/) - Provides a range of DNS and networking tools, including reverse Whois, IP location, and DNS report.

[DNSstuff](https://www.dnsstuff.com/) - Offers a comprehensive set of tools for DNS and network diagnostics, including DNS report, WHOIS lookup, traceroute, and more.

[DNSViz](https://dnsviz.net/) - A tool for visualizing the status of a DNS zone. It’s particularly useful for diagnosing DNSSEC issues but provides a detailed representation of any domain's DNS.

[DomainTools ](https://www.domaintools.com/)- Provides comprehensive information about domains, including current and historical WHOIS records, reverse WHOIS, IP tools, and more.

[**IntoDNS**](https://intodns.com/) - Checks the health and configuration of DNS and provides a detailed report of any found problems or issues.

[**DNSQuery**](http://www.dnsquery.org/) - A suite of tools for querying the DNS and other network diagnostics.

## Subdomain Enumeration

[**Sublist3r**](https://github.com/aboul3la/Sublist3r) - Enumerates subdomains using search engines and various services.

```bash
# Enumerates subdomains of example.com
sublist3r -d example.com

# Enumerates subdomains and scans for open ports 80 and 443
sublist3r -d example.com -p 80,443

# Enumerates subdomains using the Bing search engine
sublist3r -d example.com -e Bing

# Saves the enumerated subdomains to output.txt
sublist3r -d example.com -o output.txt

# Runs in verbose mode providing detailed information
sublist3r -v -d example.com
```

[**DNSdumpster**](https://dnsdumpster.com/) **-** Discovers DNS servers, MX records, and subdomains related to a domain.

[**Amass**](https://github.com/owasp-amass/amass) - Uses a variety of techniques including querying public data sources and passive DNS to enumerate subdomains. While it can perform active scanning, it also has a passive mode that strictly uses external data sources.

<pre class="language-bash"><code class="lang-bash"><strong># This command runs Amass in passive mode to enumerate subdomains of example.com.
</strong>amass enum --passive -d example.com
</code></pre>

**ThreatCrowd** - A search engine for threats, providing data on domains, IPs, and more, including subdomains.

[**Spyse**](https://spyse.com/) **-** Collects data about internet assets, including a comprehensive list of subdomains for a given domain.

## Domain Certificate Enumeration

[**crt.sh**](https://crt.sh/) - A search engine for certificates, crt.sh lets you look up SSL/TLS certificates issued for a given domain or IP address by querying the public Certificate Transparency logs.

[**SSL Certificates Chain Checker (SSL Labs)**](https://www.ssllabs.com/ssltest/) **-** This tool by Qualys SSL Labs checks the validity and chain of trust of SSL/TLS certificates for a domain.

[**CertSpotter**](https://sslmate.com/certspotter/) - CertSpotter monitors Certificate Transparency logs to notify you when new certificates are issued for your domains, helping detect misissued certificates and prevent phishing.

[**Google's Certificate Transparency**](https://github.com/google/certificate-transparency) **-** Google's Certificate Transparency project aims to fix structural flaws in the SSL certificate system by providing an open framework for monitoring and auditing SSL certificates.

**OpenSSL** - is a robust, full-featured open-source toolkit that implements the Secure Sockets Layer (SSL) and Transport Layer Security (TLS) protocols. It can be used for certificate enumeration among other things.

```bash
# Connects to the specified domain and retrieves the SSL/TLS certificate.
openssl s_client -showcerts -connect example.com:443

# Retrieves the validity dates of the domain's SSL/TLS certificate.
echo | openssl s_client -connect example.com:443 2>/dev/null | openssl x509 -noout -dates

# Displays the serial number of the domain's certificate.
openssl s_client -connect example.com:443 | openssl x509 -noout -serial

# Shows who issued the domain's SSL/TLS certificate.
openssl s_client -connect example.com:443 | openssl x509 -noout -issuer

# Verifies a certificate (example.pem) against a specific Certificate Authority (ca.pem).
openssl verify -CAfile ca.pem example.pem
```

## Analyzing Digital Footprints

[**Security Trails**](https://securitytrails.com/) - Offers historical data about domains, DNS records, subdomains, and associated IPs.

[**Wayback Machine**](https://web.archive.org/) **-** Views archived versions of web pages to understand past content and configurations.

[Netcraft Site Report](https://sitereport.netcraft.com/) - Provides information on the technology used by a domain, its hosting history, and risk ratings.

[**BuiltWith**](https://builtwith.com/) - To determine the technology stack of a website, including web servers, frameworks, analytics tools, and more.
