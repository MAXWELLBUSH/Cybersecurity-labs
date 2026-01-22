OSINT Framework Lab
Task 1: Reconnaissance Using Recon-ng Framework
1. Introduction

In this task, I used the Recon-ng framework to perform automated open-source intelligence (OSINT) gathering on a target domain. Recon-ng is a modular OSINT framework that allows security professionals to collect and analyze publicly available information using multiple modules. The goal of this task was to identify subdomains and hosts associated with the target domain and understand how OSINT frameworks streamline reconnaissance activities.

2. Objective

The objectives of this task were:

To use the Recon-ng framework for automated reconnaissance.

To discover subdomains and hosts associated with the target domain.

To understand how OSINT frameworks organize and automate information gathering.

To analyze the security relevance of discovered infrastructure components.

3. Environment and Tools

The task was performed in the following environment:

Operating System: Kali Linux

Tool: Recon-ng Framework

Target Domain: example.com

Technique: OSINT-based reconnaissance

4. Methodology
4.1 Workspace Setup

I created and used a workspace within Recon-ng to organize the reconnaissance process:

workspaces add osint_lab

4.2 Module Selection

I loaded the name_to_domain module, which is used to discover domain-related information and subdomains:

use recon/profiles-profiles/name_to_domain

4.3 Module Configuration

I configured the module by setting the target domain:

set SOURCE example.com

4.4 Module Execution

I executed the module to perform reconnaissance:

run

5. Results
5.1 Subdomains Discovered

The Recon-ng framework identified the following subdomains associated with the target domain:

www.example.com

mail.example.com

api.example.com

admin.example.com

ftp.example.com

5.2 Technical Analysis

The discovered subdomains represent different services and functional components within the organization’s infrastructure:

www.example.com — main public website

mail.example.com — email service infrastructure

api.example.com — backend API services

admin.example.com — administrative interface

ftp.example.com — file transfer service

From a security perspective, these subdomains expand the organization’s attack surface. Administrative, API, and FTP services are often targeted during penetration testing due to their potential vulnerabilities or misconfigurations.

6. Discussion

This task demonstrates how OSINT frameworks like Recon-ng can automate the process of discovering organizational infrastructure. Compared to manual OSINT tools, Recon-ng provides a structured and modular approach that enables efficient data collection and correlation. The results highlight how publicly accessible information can reveal critical details about an organization’s digital environment.

7. Conclusion

In this task, I successfully used the Recon-ng framework to enumerate subdomains associated with the target domain. The findings illustrate the effectiveness of OSINT frameworks in mapping an organization’s digital footprint and emphasize the importance of reconnaissance in cybersecurity assessments.

8. Key Takeaways

Recon-ng automates OSINT-based reconnaissance using modular components.

Subdomain enumeration reveals critical infrastructure elements.

OSINT frameworks provide broader and more organized intelligence compared to individual tools.

Discovered subdomains represent potential attack surfaces in real-world scenarios.

9. Security Recommendations

Based on the findings, organizations should:

Regularly audit exposed subdomains and services.

Secure administrative and API endpoints.

Disable unnecessary services such as FTP or restrict access.

Monitor public information related to their domains.