# API and Endpoint Analysis:

Active web application reconnaissance focused on API and Endpoint Analysis is crucial for uncovering potential vulnerabilities in web applications' backend services.

## API and Endpoint Analysis Tools

[**Postman**](https://www.postman.com/)**:** A popular tool for API testing that allows sending HTTP requests and analyzing responses.

{% embed url="https://www.youtube.com/watch?list=PLd92v1QxPOprsg5fTjGBApq4rpb0G-N8L&v=rdxVgV8dOnQ" %}

**Swagger UI:** Helps visualize and interact with API resources without writing any custom logic.

**Burp Suite:** Offers functionality to analyze and modify web application traffic, including API calls.

[**Insomnia**](https://insomnia.rest/)**:** A modern, beautiful, and open-source API client.

[**Paw** ](https://paw.cloud/)**(Mac Only):** A full-featured HTTP client that lets you test and describe the APIs you build or consume.

**Advanced REST Client (ARC):** An open-source tool for working with web APIs; offers a way to test HTTP requests.

**Fiddler:** A free web debugging tool for logging HTTP/S traffic.

[**Curl**](https://curl.se/) **(CLI-based):** A command-line tool for getting or sending data using URL syntax.

```bash
curl -X GET http://example.com/api
# Performs a GET request to the specified API endpoint.
curl -X POST -d '{"key1":"value1"}' http://example.com/api
# Sends a POST request with JSON data.
curl -X PUT -d 'data' http://example.com/api/1
# Sends a PUT request to update data.
curl -H "Content-Type: application/json" -X POST -d @filename.json http://example.com/api
# Sends data from a file as a POST request.
curl -o output.html http://example.com
# Downloads and saves the output to a file.
```

[**SoapUI**](https://www.soapui.org/)**:** Open source tool for testing SOAP and REST APIs.

[**REST-Assured**](https://rest-assured.io/) **(Java library):** Java DSL for easy testing of REST services.

**Apigee:** Provides API management and predictive analytics software.

**HTTPie (CLI-based):** A user-friendly HTTP client, a modern alternative to curl and wget.

```bash
http GET http://example.com/api/resource
# Fetches a resource using GET request.
http POST http://example.com/api/resource key=value
# Sends a POST request with data.
http --json POST http://example.com/api/resource name=John
# Sends a JSON POST request.
http --form POST http://example.com/api/resource name='John Doe'
# Submits form data.
http --download GET http://example.com/image.jpg
# Downloads a file.
```

**Charles Proxy:** Web debugging tool to monitor HTTP and HTTPS traffic between a client and server.

[**Mitmproxy** ](https://mitmproxy.org/)**(CLI-based):** An interactive HTTPS proxy for intercepting and modifying HTTP traffic.

```bash
mitmproxy
# Runs the mitmproxy interactive interface.
mitmdump
# Runs mitmproxy in a non-interactive mode, dumping traffic.
mitmweb
# Runs the mitmproxy with a web-based interface.
mitmproxy -w outfile
# Records traffic to a file.
mitmproxy -r infile
# Reads traffic from a file.
```

**Wireshark:** Network protocol analyzer used for network troubleshooting and analysis.

**JMeter:** Application designed to load test functional behavior and measure performance of web applications.

[**RedBot**](https://redbot.org/)**:** Web-based tool to check how HTTP resources are served and cached.

**OWASP ZAP API Scan (CLI-based):** Automated scanner for finding vulnerabilities in web APIs.

```bash
zap-api-scan.py -t http://example.com/api/swagger.json
# Scans API defined in Swagger definition.
`zap-api-scan.py -t http://example.com/api /OpenAPI`
# Scans API defined in an OpenAPI specification.
zap-api-san.py -f openapi -t http://example.com/api/openapi.yaml
# Specifies the format of the API definition.
zap-api-scan.py -r report.html -t http://example.com/api
# Generates an HTML report of the scan.
zap-api-scan.py -z "-config scanner.attackOnStart=true" -t http://example.com/api
# Sets additional ZAP configuration parameters.
```

**Telerik Fiddler:** Captures HTTP and HTTPS traffic and logs it for the user to review.

[**API Fortress**](https://apifortress.com/)**:** Automated API testing and monitoring platform.
