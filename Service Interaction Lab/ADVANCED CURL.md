📘 README — Advanced CURL
1. Introduction

In this task, I used advanced curl commands to interact with web services and analyze HTTP responses. Curl is a powerful tool for sending customized HTTP requests and testing web applications.

2. Objective

The objective of this task was to:

Use advanced curl options to send HTTP requests.

Analyze server responses and headers.

Simulate different client behaviors.

3. Tools Used

Curl

Kali Linux terminal

4. Task Execution
4.1 Verbose HTTP Request
Command Used:
curl -v http://192.168.56.105

4.2 Sending Custom Headers
Command Used:
curl -H "User-Agent: PentestLab" http://192.168.56.105

4.3 Requesting Only Headers
Command Used:
curl -I http://192.168.56.105

4.4 Sending POST Request
Command Used:
curl -X POST http://192.168.56.105 -d "username=test&password=test"

5. Analysis

Using advanced curl options allowed me to:

Inspect HTTP communication in detail.

Simulate attacker-like requests.

Identify how servers handle different HTTP methods and headers.

6. Conclusion

In this lab, I successfully used advanced curl techniques to interact with web services. This task demonstrated the importance of curl in penetration testing and web application analysis.