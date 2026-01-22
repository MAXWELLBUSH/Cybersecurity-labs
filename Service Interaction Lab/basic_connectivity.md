📘 Service Interaction Lab – README
1. Introduction

In this lab, I explored service interaction techniques to understand how network services respond to direct connections. The main goal was to interact with different services, identify running services, and extract useful information such as banners and service responses using basic networking tools.

Service interaction is an important phase in cybersecurity because it helps attackers and defenders understand what services are exposed on a target system and what information those services reveal.

2. Objective

The objective of this lab was to:

Connect to network services using command-line tools.

Identify active services and open ports.

Perform banner grabbing to collect service information.

Understand how different protocols respond to client requests.

3. Tools Used

The following tools were used during the lab:

Netcat (nc)

Telnet (telnet)

Kali Linux terminal environment

4. Task 1 – Basic Connectivity Using Netcat (nc)
4.1 Command Executed
nc -v 192.168.56.101 21

4.2 Result Observed

The connection to the target IP address on port 21 was successful. The server returned an FTP banner indicating that the FTP service was running and reachable.

Example output:

Connection to 192.168.56.101 21 port [tcp/ftp] succeeded!
220 FTP Server Ready

4.3 Explanation

I used netcat with the verbose option (-v) to connect to the FTP service. The returned banner message confirmed the presence of an FTP server. This technique is known as banner grabbing and is useful for identifying service types and versions during reconnaissance.

5. Task 2 – Service Interaction Using Telnet
5.1 Command Executed
telnet 192.168.56.103 23

5.2 Result Observed

The connection to the Telnet service on port 23 was successful. The server responded with a welcome message, confirming that the Telnet service was active.

Example output:

Trying 192.168.56.103...
Connected to 192.168.56.103.
Welcome to Telnet Service

5.3 Explanation

I used the telnet tool to connect to a remote Telnet service. The successful connection and banner response demonstrated how telnet can be used to interact with remote services and gather information about running protocols.

6. Security Relevance

Service interaction is a critical step in penetration testing and network security assessments because:

It helps identify exposed services and open ports.

Banner information can reveal software versions and configurations.

Attackers can use this information to find vulnerabilities.

Defenders can use it to harden systems and reduce attack surfaces.

7. Conclusion

In this lab, I successfully interacted with multiple network services using netcat and telnet. I identified active services and collected banner information through direct connections. This exercise demonstrated how service interaction and banner grabbing are essential techniques in cybersecurity reconnaissance and enumeration.