📘 README — HTTP Header Analysis
1. Introduction

In this task, I analyzed HTTP headers to identify information disclosed by a web server. HTTP headers provide metadata about the server, content type, security policies, and technologies used.

2. Objective

The objective of this task was to:

Retrieve HTTP headers from a web server.

Identify server information and configurations.

Understand the security implications of exposed headers.

3. Tools Used

Curl

Netcat

Kali Linux terminal

4. Task Execution
4.1 Retrieving HTTP Headers Using Curl
Command Used:
curl -I http://192.168.56.105

Example Output:
HTTP/1.1 200 OK
Server: nginx
Content-Type: text/html
Date: Thu, 22 Jan 2026

4.2 Retrieving Headers Using Netcat
Command Used:
nc 192.168.56.105 80

Request Sent:
HEAD / HTTP/1.1
Host: example.com

5. Analysis

The headers revealed:

Server type (e.g., nginx, Apache)

HTTP status codes

Content type

Date and response metadata

Such information can help attackers identify technologies and potential vulnerabilities.

6. Conclusion

In this lab, I successfully analyzed HTTP headers using curl and netcat. This task highlighted how HTTP headers can reveal critical information about web servers and their configurations.