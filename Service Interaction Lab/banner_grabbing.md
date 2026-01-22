📘 Banner Grabbing Lab – README
1. Introduction

In this task, I performed banner grabbing to identify running network services and extract information from them. Banner grabbing is a technique used in cybersecurity to collect service details such as service type, software version, and protocol information by directly interacting with open ports.

2. Objective

The objective of this task was to:

Connect to different network services.

Retrieve service banners using netcat and telnet.

Identify service types and software versions.

Understand the importance of banner information in reconnaissance.

3. Tools Used

Netcat (nc)

Telnet

Kali Linux terminal

4. Task Execution
4.1 FTP Banner Grabbing
Command Used:
nc -v 192.168.56.101 21

Result:

The FTP server responded with a banner message indicating that the FTP service was active.

Analysis:

The banner revealed the presence of an FTP service and provided information about the server software. This information can be used to identify potential vulnerabilities related to the FTP service.

4.2 SSH Banner Grabbing
Command Used:
nc -v 192.168.56.102 22

Result:

The SSH server returned a banner containing the OpenSSH version.

Analysis:

The SSH banner disclosed the SSH protocol version and software version. Such information is useful for identifying outdated or vulnerable SSH implementations.

4.3 SMTP Banner Grabbing
Command Used:
nc -v 192.168.56.104 25

Result:

The SMTP server responded with a mail service banner.

Analysis:

The SMTP banner confirmed that an email service was running on the target system. Attackers can use this information to attempt further enumeration or exploitation.

4.4 HTTP Banner Grabbing
Command Used:
nc -v 192.168.56.105 80


Manual HTTP request:

GET / HTTP/1.1
Host: example.com

Result:

The web server responded with HTTP headers and content.

Analysis:

The HTTP response revealed information about the web server, including the server type and protocol details. This information is useful for identifying web technologies and potential attack vectors.

4.5 Telnet Banner Grabbing
Command Used:
telnet 192.168.56.106 110

Result:

The POP3 server returned a welcome banner.

Analysis:

The banner confirmed that a POP3 service was running. Banner information can help identify service versions and security weaknesses.

5. Security Significance

Banner grabbing is important in cybersecurity because:

It helps identify exposed services and open ports.

It reveals software versions and configurations.

It assists in vulnerability assessment and exploitation planning.

It supports defenders in identifying unnecessary or insecure services.

6. Conclusion

In this lab, I successfully performed banner grabbing using netcat and telnet. I identified multiple running services and extracted banner information from them. This task demonstrated how banner grabbing plays a critical role in the reconnaissance and enumeration phases of penetration testing.