DNS Enumeration with dig
📌 Overview

This project demonstrates DNS enumeration using the dig tool, a fundamental technique in asset discovery and reconnaissance within cybersecurity and penetration testing.

DNS enumeration helps identify:

Domain IP addresses

Mail servers

Name servers

Security-related configurations (SPF, DKIM, etc.)

Understanding DNS records is critical because DNS is often the first point of information leakage attackers exploit.

🎯 Objective

The purpose of this lab is to:

Learn how DNS works at a practical level

Use dig to query different DNS record types

Understand how attackers and defenders use DNS information

Build a strong foundation for further asset discovery tools (Amass, Subfinder, Shodan)

🛠 Tool Used: dig
What is dig?

dig (Domain Information Groper) is a command-line DNS lookup tool used to query DNS servers and retrieve information about domain records.

It is commonly used by:

Network administrators

Security analysts

Penetration testers

📚 DNS Records Explained

DNS records store information about a domain. This lab focuses on the following:

1️⃣ A Record (Address Record)

Purpose:
Maps a domain name to an IPv4 address.

Command:

dig example.com


Example Output:

example.com. 86400 IN A 93.184.216.34


Meaning:
The domain example.com resolves to the IP address 93.184.216.34.

Security relevance:

Reveals server IPs

Helps attackers identify hosting infrastructure

2️⃣ MX Record (Mail Exchange Record)

Purpose:
Specifies which mail servers receive email for the domain.

Command:

dig example.com MX


Example Output:

example.com. 86400 IN MX 10 mail.example.com.
example.com. 86400 IN MX 20 mail2.example.com.


Meaning:

Emails sent to @example.com are delivered to these mail servers

Lower number = higher priority

Security relevance:

Mail servers are common attack targets

Can be abused for phishing, spoofing, or spam if misconfigured

3️⃣ TXT Record (Text Record)

Purpose:
Stores arbitrary text data, often used for email security and domain verification.

Command:

dig example.com TXT


Example Output:

"v=spf1 include:_spf.example.com ~all"


Meaning:

This is an SPF record

It defines which servers are allowed to send email on behalf of the domain

Security relevance:

Helps prevent email spoofing

Missing or weak TXT records increase phishing risk

4️⃣ NS Record (Name Server Record)

Purpose:
Identifies the authoritative DNS servers for the domain.

Command:

dig example.com NS


Example Output:

example.com. 86400 IN NS ns1.example.com.
example.com. 86400 IN NS ns2.example.com.


Meaning:

These servers control all DNS records for the domain

Security relevance:

Attackers target name servers for misconfigurations

Enables DNS zone transfer attempts if unsecured

🧠 Why DNS Enumeration Matters in Cybersecurity

DNS enumeration allows attackers to:

Discover infrastructure details

Identify exposed services

Map attack surfaces before exploitation

Defenders use it to:

Audit DNS configurations

Identify misconfigurations

Strengthen domain security

⚠️ Ethical Notice

This lab is performed on example.com, a domain reserved for documentation and testing.

🔒 Do not perform DNS enumeration on domains you do not own or have permission to test.