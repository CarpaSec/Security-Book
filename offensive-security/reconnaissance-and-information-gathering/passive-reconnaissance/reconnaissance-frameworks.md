# Reconnaissance Frameworks

Reconnaissance frameworks are specialized tools used in cybersecurity to systematically gather information about a target system, network, or organization without direct interaction. They are integral to the preparatory phase of penetration testing, also known as the information gathering phase. These frameworks automate the collection of public data that can help identify potential vulnerabilities and understand the security posture of a target.

## Recon-NG

<details>

<summary>Recon-NG</summary>

Recon-ng is a full-featured Web Reconnaissance framework written in Python. It has a similar interface to Metasploit, making it intuitive to those familiar with the Metasploit framework. Recon-ng is modular and has a variety of modules that can perform a multitude of reconnaissance tasks. It’s great for gathering data from open-source resources and integrates with various third-party services and APIs.

**Key Features:**

* Extensive module library for different reconnaissance tasks.
* Interactive shell for running and chaining modules.
* Ability to export findings in various formats.

Resources:&#x20;

* [GitHub Link](https://github.com/lanmaster53/recon-ng) to Recon-NG.&#x20;
* [Recon-ng: An Open Source Reconnaissance Tool](https://securitytrails.com/blog/recon-ng)
* [Recon-NG Tutorial](https://hackertarget.com/recon-ng-tutorial/)
* Check out the playlist below for a deep dive (it's free)&#x20;

</details>

{% embed url="https://www.youtube.com/watch?list=PLBf0hzazHTGOg9taK90uFjdcb8UgGfRKZ&v=1RCqOhb0yxE" %}

## Maltego

<details>

<summary>Maltego </summary>

Maltego is an interactive data mining tool that renders directed graphs for link analysis. It's an incredibly powerful tool for exploring relationships and networks between information and entities on the internet, such as people, companies, organizations, websites, domains, network infrastructure, and social network connections.

**Key Features:**

* Visual link analysis and interactive graphs.
* Integration with a wide range of data sources.
* Transformations for automating the mining and display of information.

Resource:&#x20;

* [Maltego Main Site](https://www.maltego.com/)
* [Maltego | Kali Linux Tools](https://www.kali.org/tools/maltego/)
* [How to Use Maltego: A Beginner’s Guide to OSINT Analysis](https://www.stationx.net/how-to-use-maltego/)

</details>

{% embed url="https://www.youtube.com/watch?pp=ygUHbWFsdGVnbw==&v=hfLpvyMscXI" %}

## SpiderFoot

<details>

<summary>SpiderFoot</summary>

SpiderFoot is an open-source intelligence automation tool (OSINT). It automates the process of gathering intelligence on a given target, whether that target is a domain name, hostname, IP address, or network subnet. SpiderFoot can query over 100 different public data sources and is available both as a web-based service and as a standalone scriptable Python-based software.

**Key Features:**

* Extensive data source integration for thorough reconnaissance.
* Automation of OSINT collection on multiple targets.
* Results can be exported in various formats and visualized graphically.

**Resources:**&#x20;

* [SpiderFoot – A Automate OSINT Framework in Kali Linux](https://www.geeksforgeeks.org/spiderfoot-a-automate-osint-framework-in-kali-linux/)
* [SpiderFoot GitHub](https://github.com/smicallef/spiderfoot)

</details>

{% embed url="https://www.youtube.com/watch?v=GL4IwRCU7EM" %}

## theHarvester



<details>

<summary>theHarvester</summary>

**Description:** theHarvester is a tool designed for open source intelligence (OSINT) and reconnaissance, particularly useful for early stages of a penetration test. It's designed to gather information about emails, subdomains, hosts, employee names, open ports, and banners from different public sources like search engines and PGP key databases.

**Key Features:**

* Simple command-line interface.
* Quick enumeration of emails, subdomains, and hosts.
* Supports various search engines and sources for data collection.

**Resources:**

* [GitHub Repo](https://github.com/laramies/theHarvester)
* [FootPrinting/Reconnaissance using tools the harvester](https://medium.com/@nancyjohn\_95536/footprinting-reconnaissance-using-tools-the-harvester-2006361a9f94)
* [OSINT analysis — SpiderFoot & theharvester (Information Gathering)](https://systemweakness.com/osint-analysis-spiderfoot-theharvester-information-gathering-5de59746c5c7)
* To gather emails and subdomains from a particular domain, you might use `theHarvester -d targetdomain.com -b google`.

</details>

{% embed url="https://www.youtube.com/watch?pp=ygUcdGhlaGFydmVzdGVyIHJlY29uIGZyYW1ld29yaw==&v=cDryilcK39c" %}

## Shodan

<details>

<summary>Shodan</summary>

Shodan is not a framework but a search engine that lets the user find specific types of computers connected to the internet using a variety of filters. Although it’s a standalone service, it’s often used within reconnaissance frameworks or in the reconnaissance phase to find devices, servers, and even IoT devices that are publicly accessible on the internet.

**Key Features:**

* Finds devices connected to the internet.
* Can filter by device type, country, port, operating system, and more.
* Offers powerful API integration for custom tools and scripts.

Resources:&#x20;

* [Main site](https://www.shodan.io/)
* [What Is Shodan? How to Use It & How to Stay Protected \[2024\]](https://www.safetydetectives.com/blog/what-is-shodan-and-how-to-use-it-most-effectively/)

</details>

{% embed url="https://www.youtube.com/watch?pp=ygUHc2hvZGFuIA==&v=v2EdwgX72PQ" %}
