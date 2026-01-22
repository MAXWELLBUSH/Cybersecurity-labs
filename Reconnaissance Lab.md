🛡️ Reconnaissance Lab Report: Domain, Subdomain, and IP Enumeration
1. Introduction

In this lab, I conducted reconnaissance on a target organization by identifying its domain, subdomains, and IP addresses. The purpose of this exercise was to understand how attackers gather information about a target and how such information can be leveraged to identify potential attack vectors.

Reconnaissance is a critical phase in penetration testing because it helps in mapping the target’s attack surface before attempting exploitation.

2. Objectives

In this lab, I aimed to:

Identify the primary domain of the target organization

Enumerate subdomains associated with the domain

Resolve IP addresses linked to the domain and subdomains

Analyze how the discovered information could be exploited by attackers

3. Methodology
3.1 Domain Enumeration

I identified the main domain using DNS lookup techniques and OSINT tools such as nslookup, dig, and WHOIS queries.
This helped me determine the organization’s primary online presence and DNS configuration.

3.2 Subdomain Enumeration

I performed subdomain enumeration using tools such as Sublist3r and Amass, as well as certificate transparency logs.
Through this process, I discovered multiple subdomains, including development, administrative, and service-related endpoints.

These subdomains revealed additional systems that were not directly visible from the main website, thereby expanding the attack surface.

3.3 IP Address Resolution

I resolved the IP addresses associated with the domain and its subdomains using DNS queries and network scanning tools such as ping and nmap.
This allowed me to identify the servers hosting the organization’s services and analyze their network exposure.

4. Exploitation Potential
4.1 Domain Exploitation

By knowing the main domain, I could:

Analyze the web application for vulnerabilities such as SQL Injection, XSS, and authentication flaws

Identify technologies and frameworks used by the application

Map sensitive endpoints such as login pages and APIs

The domain serves as the primary entry point for web-based attacks.

4.2 Subdomain Exploitation

The discovered subdomains could be exploited in several ways:

Targeting poorly secured development or testing environments

Identifying exposed admin panels and internal tools

Exploiting outdated or misconfigured applications

Performing subdomain takeover attacks

Subdomains often have weaker security controls, making them attractive targets for attackers.

4.3 IP Address Exploitation

The identified IP addresses enabled network-level reconnaissance and exploitation, including:

Port scanning to identify open services (HTTP, SSH, FTP, SMTP, etc.)

Detecting vulnerable services and outdated software versions

Exploiting misconfigured services and weak authentication mechanisms

Launching denial-of-service attacks

IP addresses reveal the underlying infrastructure that supports the organization’s digital services.

5. Security Implications

From this lab, I learned that domain, subdomain, and IP information significantly reduce the effort required by attackers to compromise an organization.
By correlating these assets, an attacker can effectively map the target’s infrastructure and identify high-risk entry points.

This highlights the importance of continuous asset monitoring, proper configuration, and security hardening.

6. Conclusion

In conclusion, this lab demonstrated how reconnaissance plays a crucial role in cybersecurity.
Understanding how attackers gather and exploit domain, subdomain, and IP information is essential for building strong defensive strategies.