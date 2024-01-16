# Analyzing Client Side Code

## JavaScript Analysis Tools

**JavaScript Deobfuscator (Browser Extension):** Deobfuscates and beautifies JavaScript code to make it readable.

* **Website:** Available as a browser extension for Chrome and Firefox.

[**JSNice**](http://www.jsnice.org/)**:** Predicts and renames variables, deobfuscates and beautifies JavaScript.

[**JSHint**](https://jshint.com/)**:** A static code analysis tool used in software development for checking JavaScript code quality.

[**ESLint** ](https://eslint.org/)**(CLI-based):** A pluggable linting utility for JavaScript.

```bash
eslint file.js
# Lints file.js.
eslint --init
# Sets up ESLint for a project.
eslint --fix file.js
# Automatically fixes problems in file.js.
eslint -f json file.js > report.json
# Outputs results in JSON format.
eslint --debug file.js
# Runs ESLint in debug mode for file.js.
```

**UglifyJS (CLI-based):** A JavaScript parser, minifier, compressor, or beautifier toolkit.

```bash
uglifyjs file.js -o file.min.js
# Minifies file.js.
uglifyjs file.js -b
# Beautifies file.js.
uglifyjs file.js -m
# Mangles names in file.js.
uglifyjs file.js -c
# Compresses file.js.
uglifyjs file.js --source-map
# Generates a source map for file.js.
```

{% embed url="https://www.youtube.com/watch?pp=ygUZSmF2YVNjcmlwdCBBbmFseXNpcyBUb29scw==&v=ssRo5nVOvrQ" %}

## HTML and DOM Inspection Tools

**Chrome Developer Tools (DevTools):** Provides deep access and insight into the web pages' front-end.

* &#x20;Built into Google Chrome Browser.

[**Firebug**](http://getfirebug.com/)**:** A tool for live debugging, editing, and monitoring of web pages' CSS, HTML, DOM, and JavaScript.

* (Note: Firebug is no longer actively maintained, as many of its features have been integrated into browser developer tools.)

**DOM Inspector (Browser Extension):** Inspects the DOM of web pages.

**HTML Validator (Browser Extension):** Validates HTML of web pages and highlights errors.

**WAVE (Web Accessibility Evaluation Tool):** Evaluates web page accessibility by identifying errors in HTML and DOM structure.

{% embed url="https://www.youtube.com/watch?pp=ygUdSFRNTCBhbmQgRE9NIEluc3BlY3Rpb24gVG9vbHM=&v=Gk6BljF60RI" %}

## CSS Analysis Tools

**CSS Validator:** Checks the validity and compliance of CSS code on web pages.

[**Stylelint** ](https://stylelint.io/)**(CLI-based):** A modern linter for CSS and stylesheets.

```bash
stylelint "src/**/*.css"
# Lints all CSS files in the src directory.
stylelint "src/**/*.css" --fix
# Automatically fixes problems in CSS files.
stylelint --config myconfig.json "src/**/*.css"
# Uses a custom configuration file.
stylelint "src/**/*.css" --formatter json
# Outputs results in JSON format.
stylelint "src/**/*.css" --ignore-path .gitignore
# Ignores files listed in .gitignore.
```

**Sass Lint:** Linter for Sass and SCSS files.

[**PurifyCSS**](https://purifycss.online/)**:** Removes unused CSS, reducing file size and improving load times.

[**CSS Stats**](https://cssstats.com/)**:** Provides analytics and visualization of CSS file sizes, rules, and selectors.

{% embed url="https://www.youtube.com/watch?pp=ygUSQ1NTIEFuYWx5c2lzIFRvb2xz&v=oRKlKhFt2Rg" %}

## Code Review and Debugging Tools

[**SonarQube**](https://www.sonarqube.org/)**:** Analyzes source code for bugs, vulnerabilities, and code smells in various programming languages.

**Visual Studio Code:** Source code editor with built-in debugging and Git control.

**Web Developer (Browser Extension):** Adds a toolbar with various web development tools to the browser.

**Debugger for Chrome (Visual Studio Code Extension):** Allows debugging JavaScript code in the Chrome browser from within Visual Studio Code.

[**Tampermonkey**](https://www.tampermonkey.net/) **(Browser Extension):** Userscript manager for running and managing JavaScript scripts on web pages.

{% embed url="https://www.youtube.com/watch?pp=ygUfQ29kZSBSZXZpZXcgYW5kIERlYnVnZ2luZyBUb29scw==&v=Y9sp8gONv9M" %}

## Browser Console and Network Analysis

**Chrome Developer Tools (DevTools):** Provides deep insights into web applications, including network traffic, performance, and JavaScript debugging.

* Built into Google Chrome Browser.

**Firefox Developer Tools:** A set of debugging tools built into Firefox, similar to Chrome DevTools.

**Fiddler:** Captures HTTP and HTTPS traffic between the web and your machine for inspection and debugging.

**Wireshark:** Network protocol analyzer used for network troubleshooting, analysis, and protocol development.

[**HTTP Toolkit**](https://httptoolkit.tech/)**:** Intercepts, debugs, and builds HTTP(S) with a suite of powerful tools.

## JavaScript Debugging and Profiling

**Node.js Inspector:** Debugs and profiles JavaScript code running in Node.js.

**LightHouse:** Automated tool by Google for improving the quality of web pages. It audits performance, accessibility, and more.

**Debugger for Firefox (Visual Studio Code Extension):** Enables debugging of web applications running in Firefox from within Visual Studio Code.

**Chrome DevTools Profiler:** Profiles JavaScript performance in Chrome to find and fix performance bottlenecks.

## Accessibility Testing

**axe Accessibility Checker (Browser Extension):** Accessibility auditing tool for web applications.

**WAVE (Web Accessibility Evaluation Tool):** Evaluates the accessibility of web content.
