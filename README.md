# Nessus-Scanning

## Project Overview

 **This project demonstrates the use of Nessus for network and web application security assessments. The objective is to identify vulnerabilities in a controlled lab environment using different Nessus scan types** 

## Prerequisites
## Step 1: Download & Install Nessus
**Purpose: Set up Nessus on your system.**
**Steps:Go to the official Tenable Nessus download page: https://www.tenable.com/products/nessus.**
 **Enter credientials or register** 
![image](https://github.com/user-attachments/assets/3e3be7a9-e434-474c-b4c1-c09cf17d2b82)
**Select the version compatible with your OS (e.g., Kali Linux → Nessus-10.x-debian-amd64.deb).**
![image](https://github.com/user-attachments/assets/47d94dde-4fde-481d-a5b1-048a50072eca)
**Open a terminal in Kali Linux and navigate to the download directory**
**Run the following command to install Nessus:```sudo dpkg -i ```**

## Start Nessus service: ```sudo systemctl start nessusd```

Enable Nessus to start on boot:
sudo systemctl enable nessusd
Open a web browser and navigate to https://localhost:8834 to complete the setup.
Create a Nessus account and activate it using the activation code from the Tenable website.
Wait for the plugin update to complete (~10-20 minutes).


 **Virtual Lab Setup with vulnerable machines:**

 **Metasploitable 2 (for network vulnerability scanning)**

 **OWASP Broken Web Apps (BWA) or DVWA (for web application scanning)**

 **VirtualBox or VMware to run the VMs.**

📖 Step 1: Host Discovery Scan (Network Mapping)

Purpose: Identify active hosts and open ports on the network.

Steps:

Open Nessus and select New Scan → Host Discovery.

Enter the target IP range of your lab setup (e.g., 192.168.1.0/24).

Under Scan Settings, select:

Ping Hosts → Enabled

Scan Common Ports → Enabled

Click Save and then Launch Scan.

📸 Take Screenshot of scan results.

📖 Step 2: Basic Network Scan

Purpose: Identify open ports, services, and basic vulnerabilities.

Steps:

Select New Scan → Basic Network Scan.

Enter the target machine's IP (e.g., Metasploitable 2: 192.168.1.100).

Under Discovery, select Port Scan (Common Ports).

Under Assessment, enable:

Check for Vulnerabilities

Check for Misconfigurations

Click Save and Launch Scan.

📸 Take Screenshot of scan results and note high-severity vulnerabilities.

📖 Step 3: Advanced Vulnerability Scan

Purpose: Perform an in-depth security assessment of a target system.

Steps:

Select New Scan → Advanced Scan.

Enter the target IP (Metasploitable 2 or Windows VM).

Under Discovery, select Port Scan (All Ports).

Under Assessment, enable:

Check for Known Vulnerabilities

Configuration Audits

Malware Detection (if available)

(Optional) Under Credentials, add SSH or Windows credentials for a deeper scan.

Click Save & Launch Scan.

📸 Take Screenshot of scan report with vulnerability details.

📖 Step 4: Web Application Scan (DVWA or OWASP BWA)

Purpose: Identify web vulnerabilities such as SQL Injection, XSS, and authentication flaws.

Steps:

Select New Scan → Web Application Tests.

Enter the target web application URL (e.g., http://192.168.1.105/dvwa/).

Under Discovery, select:

Port Scan (Custom) → Ports 80, 443.

Under Assessment, select Scan for All Web Vulnerabilities (Complex).

Under Credentials, select HTTP Login Form:

Username: admin

Password: password

Login URL: http://192.168.1.105/dvwa/login.php

Click Save & Launch Scan.

📸 Take Screenshot of scan results.

📖 Step 5: Documenting Results & Reporting

Purpose: Generate a professional report summarizing the findings.

Steps:

After each scan, export the results:

Click Reports → Export as PDF/CSV.

In a Markdown file (or GitHub README):

Describe the scan type.

Include key vulnerabilities found.

Attach screenshots.

Organize your results into sections:

Network Vulnerabilities (from Basic & Advanced scans)

Web Application Vulnerabilities (from OWASP/DVWA scan)

Potential Mitigations for identified issues.





