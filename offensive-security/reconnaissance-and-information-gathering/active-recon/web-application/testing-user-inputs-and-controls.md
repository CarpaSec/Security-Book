# Testing User Inputs and Controls:

Testing user inputs and controls is a crucial part of active web application reconnaissance, focusing on how the application handles user-provided data and access controls.&#x20;

## SQL Injection Testing

[**SQLmap** ](http://sqlmap.org/)**(CLI-based):** Automates the detection and exploitation of SQL injection flaws.

```bash
sqlmap -u "http://example.com/page.php?id=1"
# Test for SQL injection at the given URL.
sqlmap -u "http://example.com" --forms
# Test forms on a given URL for SQL injection.
sqlmap -u "http://example.com" --dbs
# Enumerate DBMS databases.
sqlmap -u "http://example.com" --batch
# Non-interactive mode, using default options.
sqlmap -u "http://example.com" --risk=3 --level=5
# Increase risk and level settings for more thorough testing.
```

{% embed url="https://www.youtube.com/watch?pp=ygUTc3FsbWFwIGFjdGl2ZSByZWNvbg==&v=2YD4vygeghM" %}

**jSQL Injection:** A lightweight application used to find database information from a distant server.

## Cross-Site Scripting (XSS) Testing

**XSStrike:** Designed to detect and exploit XSS vulnerabilities in web applications.

**XSSer:** Automated tool for detecting and exploiting XSS vulnerabilities.

{% embed url="https://www.youtube.com/watch?pp=ygUFeHhzZXI=&v=HZ2K-Y8fTyc" %}

## Command Injection Testing

**Commix:** Automated all-in-one tool for exploiting command injection vulnerabilities.

{% embed url="https://www.youtube.com/watch?pp=ygUZY29tbWFuZCBpbmplY3Rpb24gdGVzdGluZw==&v=UBWMLFbjPBc" %}

## Cross-Site Request Forgery (CSRF) Testing

**CSRFTester:** Tool for testing CSRF vulnerabilities in web applications.

{% embed url="https://www.youtube.com/watch?pp=ygUMY3NyZiB0ZXN0aW5n&v=TwG0Rd0hr18" %}

## Session Management Testing

**Burp Suite:** Integrated platform for performing security testing, including session management.

[**Cookie Cadger**](https://cookiecadger.com/)**:** Tool for identifying information leakage and session hijacking in network traffic.

{% embed url="https://www.youtube.com/watch?pp=ygUac2Vzc2lvbiBtYW5hZ2VtZW50IHRlc3Rpbmc=&v=zHBpJA5XfDk" %}

## Authentication Testing

**Hydra (CLI-based):** Fast network logon cracker which supports many different services.

```bash
hydra -l user -p pass ftp://192.168.0.1
# Basic FTP login test.
hydra -L userlist.txt -P passlist.txt 192.168.0.1 ssh
# SSH brute force with username and password lists.
hydra -s 80 -l admin -P passlist.txt 192.168.0.1 http-get /admin
# HTTP GET page login brute force.
hydra -l admin -p password http-post-form "http://example.com/login:user=^USER^&pass=^PASS^:Login failed"
# HTTP POST form brute force
hydra -C defaults.txt -6 http-get://[ipv6addr]/admin
# Brute force IPv6 HTTP GET with default credentials list.
```

**John the Ripper:** A fast password cracker for testing password strength and cracking encrypted passwords.

**Patator (CLI-based):** A multi-purpose brute-forcer, with a modular design and a flexible usage.

```bash
patator http_fuzz url=http://example.com/login method=POST body='user=admin&password=FILE0' 0=passwords.txt
# HTTP POST password brute-force.
patator ssh_login host=192.168.0.1 user=root password=FILE0 0=passwords.txt
# SSH brute-force login.
patator ftp_login host=192.168.0.1 user=admin password=FILE0 0=passwords.txt
# FTP brute-force login.
patator smtp_login host=192.168.0.1 user=admin password=FILE0 0=passwords.txt
# SMTP brute-force login.
patator http_fuzz url=http://example.com/search method=GET accept_cookie=1 follow=1 before_urls=http://example.com/login before_post='user=admin&password=admin' file=0 0=words.txt
# Fuzzing HTTP GET parameters.
```

**OWASP ZAP:** Features various tools for authentication testing, including brute-forcing.

**NoSQLMap:** Automated tool to audit and exploit NoSQL databases like MongoDB for weak password vulnerabilities.

## Input Validation Testing

**OWASP Amass:** In-depth Attack Surface Mapping and Asset Discovery using open-source information gathering and active reconnaissance techniques.

**Wfuzz (CLI-based):** A tool for brute-forcing web applications.

```bash
wfuzz -c -z file,wordlist.txt --hc 404 http://example.com/FUZZ
# Brute-forces directories and file names.
wfuzz -c -z file,users.txt -z file,pass.txt --sc 200 http://example.com/login.php?user=FUZZ&password=FUZ2Z
# Brute-forces username and password combinations.
wfuzz -c -z range,1-1000 -u http://example.com/page?id=FUZZ
# Fuzzes 'id' parameter values from 1 to 1000.
wfuzz -w wordlist.txt --hw 57 http://example.com/path/FUZZ
# Brute-force with wordlist, hiding responses with 57 words.
wfuzz -c -z file,scripts.txt -u http://example.com/js/FUZZ.js
# Fuzzing for JavaScript files.
```

**Burp Intruder (Part of Burp Suite):** A powerful tool for performing automated and customized attacks against web applications.

**SQLiPy (SQLMap Integration in Burp Suite):** Integrates SQLMap's SQL injection capabilities into Burp Suite for automated testing.

**BlindElephant:** Web Application Fingerprinter that identifies web applications' versions by comparing static files at known locations against precomputed hashes.

{% embed url="https://www.youtube.com/watch?pp=ygUYaW5wdXQgdmFsaWRhdGlvbiB0ZXN0aW5n&v=EA8-GuMZykg" %}

## Cross-Site Scripting (XSS) Testing

**XSSer:** Automated tool for detecting and exploiting XSS vulnerabilities.

**XSS Payload List:** A repository of payloads for testing XSS vulnerabilities.

[**BeEF** ](https://beefproject.com/)**(Browser Exploitation Framework):** A penetration testing tool that focuses on the web browser, exploiting XSS vulnerabilities to hook browsers and perform further attacks.

**DOMinatorPro:** An advanced tool for the analysis and identification of DOM-based Cross-Site Scripting (XSS) vulnerabilities.

**XSStrike:** Designed to detect and exploit XSS vulnerabilities in web applications.

## Cross-Site Request Forgery (CSRF) Testing

**CSRFTester:** Tool for testing CSRF vulnerabilities in web applications.

**Burp Suite (CSRF Tokens tab):** A feature within Burp Suite to test for CSRF vulnerabilities.

**OWASP CSRFGuard:** A library that implements various protections against CSRF attacks.

Session Management Testing

[**Cookie Cadger**](https://cookiecadger.com/)**:** Tool for identifying information leakage and session hijacking in network traffic.

## Other Input and Control Testing Tools

[**Paros Proxy**](https://www.parosproxy.org/)**:** A Java-based HTTP/HTTPS proxy for assessing web application vulnerability.

**Ratproxy:** A semi-automated, largely passive web application security audit tool.

**Skipfish:** An active web application security reconnaissance tool.
