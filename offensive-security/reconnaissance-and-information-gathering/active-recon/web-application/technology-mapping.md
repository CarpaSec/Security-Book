# Technology Mapping

Understanding a web application during reconnaissance involves gathering as much information as possible about its structure, functionality, and underlying technology.&#x20;

[**Wappalyzer**](https://www.wappalyzer.com/)**:** Identifies technologies on websites, such as CMS, web frameworks, server software, and analytics tools.

{% embed url="https://www.youtube.com/watch?pp=ygUKd2FwcGFseXplcg==&v=q8xx1ZRgKRo" %}

[**BuiltWith**](https://builtwith.com/)**:** Provides details about the technology stack of websites, including server information, CMS, and scripting languages.

**WhatWeb:** Identifies website technologies, including content management systems, web server platforms, and JavaScript libraries.

**Retire.js (Browser Extension):** Identifies web applications using outdated JavaScript libraries with known vulnerabilities.

**Recon-ng (Web Module):** Web reconnaissance framework with modules to identify technologies used by web applications.

* **Example Commands:**
  * `recon-ng`: Start Recon-ng.
  * `marketplace search web`: Find web modules.
  * `modules load recon/domains-hosts/builtwith`: Load BuiltWith module.
  * `options set SOURCE example.com`: Set target domain.
  * `run`: Execute the module.

**Browser Extensions like Technology Profiler and Web Tech Detector:** Browser add-ons to detect web technologies used on sites.

**Netcraft Extension:** Provides information about the sites visited including background on the site's hosting, risk ratings, and technology.

[**StackPath** ](https://www.stackpath.com/)**(Formerly MaxCDN):** Identifies Content Delivery Networks (CDNs) used by websites.

**Library Sniffer (Browser Extension):** Detects JavaScript libraries and frameworks used on web pages.

**Green:** Determines the timezone settings used by a web server, which can hint at the server's physical location or configuration settings.

**Header Check:** Analyzes HTTP response headers to determine server configuration and technologies.

[**Hexometer**](https://hexometer.com/)**:** Scans websites to detect over 2,800 website technologies and monitors for changes.

**SiteSucker (Mac App):** Automatically downloads websites and extracts their structure, including scripts, stylesheets, and other resources.

**Extension: Stylebot (Browser Extension):** Allows customization of website appearance, providing insights into CSS and web design frameworks used.

**JavaScript and CSS Code** [**Beautifier**](https://beautifier.io/)**:** Beautifies and formats obfuscated or minified JavaScript and CSS codes to understand the underlying technology better.
