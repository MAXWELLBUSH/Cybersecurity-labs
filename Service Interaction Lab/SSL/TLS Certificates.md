📘 README — SSL/TLS Certificates
1. Introduction

In this task, I examined SSL/TLS certificates to understand how encrypted communication is established between clients and servers. SSL/TLS certificates provide authentication and encryption for secure web communication.

2. Objective

The objective of this task was to:

Retrieve SSL/TLS certificate information from a server.

Analyze certificate details such as issuer, validity period, and encryption algorithms.

Understand the security role of SSL/TLS.

3. Tools Used

OpenSSL

Curl

Netcat

Kali Linux terminal

4. Task Execution
4.1 Viewing SSL Certificate Using OpenSSL
Command Used:
openssl s_client -connect 192.168.56.108:443

4.2 Checking HTTPS Response Using Curl
Command Used:
curl -v https://192.168.56.108

5. Analysis

The certificate information revealed:

Certificate issuer

Validity period

Encryption algorithms

Domain name association

This information is important in identifying misconfigured or expired certificates, which can weaken security.

6. Conclusion

In this lab, I successfully analyzed SSL/TLS certificates using OpenSSL and curl. This task demonstrated how encryption and authentication are implemented in secure web communication.