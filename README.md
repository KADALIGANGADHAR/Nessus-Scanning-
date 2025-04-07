# Nessus-Scanning

## Project Overview

- **This project demonstrates the use of Nessus for network and web application security assessments. The objective is to identify vulnerabilities in a controlled lab environment using different Nessus scan types** 

## Prerequisites
 **Virtual Lab Setup with vulnerable machines:**

- **Metasploitable 2 (for network vulnerability scanning)**

- **OWASP Broken Web Apps (BWA) or DVWA (for web application scanning)**

- **VirtualBox or VMware to run the VMs.**
## Step 1: Download & Install Nessus
**Purpose: Set up Nessus on your system.**
**Steps:Go to the official Tenable Nessus download page: https://www.tenable.com/products/nessus.**
 **Enter credientials or register** 
![image](https://github.com/user-attachments/assets/3e3be7a9-e434-474c-b4c1-c09cf17d2b82)
**Select the version compatible with your OS (e.g., Kali Linux → Nessus-10.x-debian-amd64.deb).**
![image](https://github.com/user-attachments/assets/47d94dde-4fde-481d-a5b1-048a50072eca)
- **Open a terminal in Kali Linux and navigate to the download directory**
- **Run the following command to install Nessus:```sudo dpkg -i Nessus-10.8.3-ubuntu1604_amd64.deb```**
![image](https://github.com/user-attachments/assets/7a92a9a5-cec8-4a8a-94f9-fd82d39bcb1a)
**Start Nessus service: ```sudo systemctl start nessusd```**
![image](https://github.com/user-attachments/assets/1acc60b4-6f57-453a-beed-fa4df81de540)

- **Open a web browser and navigate to https://localhost:8834 to complete the setup.**
![image](https://github.com/user-attachments/assets/fb85593f-fbf7-42f5-9114-0345cea48952)
- **Click on Accept the Risk and Continue**
![image](https://github.com/user-attachments/assets/f110215f-761c-4f0a-a067-a189d398afa9)
![image](https://github.com/user-attachments/assets/c04e51f4-5aec-45f0-b9c1-485735dbec40)
- **Click on Register for Nessus Essentials**
![image](https://github.com/user-attachments/assets/6aa70903-71b6-48df-a019-7a1b8161a27c)
- **Click on Skip**
![image](https://github.com/user-attachments/assets/77616470-2c16-41dd-b6f1-e831f584528e)
- **Create a Nessus account and activate it using the activation code from the Tenable website.**
- **During the activation processin Nessus,the activation code is sent to the registered email address associated ith your Tenable account**
![image](https://github.com/user-attachments/assets/7456e64a-0e95-43f0-8d8a-2de54d9131f4)
- **Create user name and password**
![image](https://github.com/user-attachments/assets/877640dc-8188-441b-bf6a-a355abb27b8b)
![image](https://github.com/user-attachments/assets/cd4a5f94-293c-48ed-928b-794ddf4eab2a)

- **Wait for the plugin update to complete (~10-20 minutes).**
![image](https://github.com/user-attachments/assets/32a2f786-e9f8-4f29-80f3-fa2092de4c95)
![image](https://github.com/user-attachments/assets/c1dfd9a1-6a87-48f6-8aa6-f79c617fa91e)


 
## Step 1: Basic Network Scan

**Purpose: Identify open ports, services, and basic vulnerabilities.**

- **Steps:Select New Scan → Basic Network Scan.**
![image](https://github.com/user-attachments/assets/d43cb265-4f99-4023-923c-ae4795daff81)
![image](https://github.com/user-attachments/assets/a6adae7b-f18c-40d8-8e6c-f5c148655026)

- **Enter the target machine's IP (e.g., OWASP WEB scan :192.168.235.133).and details as per below**
![image](https://github.com/user-attachments/assets/3ec022aa-608d-4911-9065-cfcb5c7e5824)
- **Click Save and Launch Scan.**
![image](https://github.com/user-attachments/assets/91d331ff-4c79-42bb-8026-ca146fc956be)
![image](https://github.com/user-attachments/assets/205a084e-1c5b-4e98-b39d-81542ffc4c25)
- **After scan it will show the scan details**
![image](https://github.com/user-attachments/assets/1e449539-2ad6-4fd6-9103-d9586f401d68)
![image](https://github.com/user-attachments/assets/bffec5bd-466a-4be9-b020-8f5f94393895)
![image](https://github.com/user-attachments/assets/e913e407-af26-4c7c-ada3-b33b2fa26fca)
- **Generate and save the report**
![image](https://github.com/user-attachments/assets/340287be-ae27-46e3-8f45-debe286449b6)

## Step 2: Host Discovery Scan (Network Mapping)

**Purpose: Identify active hosts and open ports on the network.**

- **Steps:Open Nessus and select New Scan → Host Discovery.**
![image](https://github.com/user-attachments/assets/23373846-d368-4430-b50d-c0d528807f4e)
![image](https://github.com/user-attachments/assets/5e5a2156-4b52-4c1a-b64f-8231b2f9a101)
![image](https://github.com/user-attachments/assets/08f04e58-c8b3-4604-b881-5ae7ceda6871)
![image](https://github.com/user-attachments/assets/1b70a53a-f2a0-49cf-9bac-739475dcd93c)
![image](https://github.com/user-attachments/assets/0201b6c7-1071-44ca-aed3-ac0aad7f813c)
![image](https://github.com/user-attachments/assets/5df640a1-0d1c-4052-8a4f-078018c74f7a)
![image](https://github.com/user-attachments/assets/f220e895-87cb-40c1-884d-93e837ab1bdc)
![image](https://github.com/user-attachments/assets/3ce28a9b-455d-4490-9495-dd8a389400f8)
![image](https://github.com/user-attachments/assets/81be7dc7-6a2b-4230-a4a3-5b4b0e27639c)
![image](https://github.com/user-attachments/assets/f4e76478-be97-4283-a74c-b34d28412dff)
![image](https://github.com/user-attachments/assets/a9392535-2e3e-4593-a943-77757731f76b)
![image](https://github.com/user-attachments/assets/ab939c8b-65cb-4901-9c6d-e4c2ddef43ca)
![image](https://github.com/user-attachments/assets/6bc111c1-d1ac-4210-b632-8c25d408508a)
![image](https://github.com/user-attachments/assets/b79f7ff4-d610-4b67-ad55-17b3bb4aa317)

## Step 3: Advanced Vulnerability Scan

**Purpose: Perform an in-depth security assessment of a target system.**

**Steps:Select New Scan → Advanced Scan.**
![image](https://github.com/user-attachments/assets/5f4f437c-112a-4397-80d2-7b3c30688ea3)
- **Enter the target IP.(Metasploitable 2 or Windows VM).**
- **Under Discovery, select Port Scan (All Ports).**
- **Under Assessment, enable:Check for Known Vulnerabilities**
- **Configuration Audits**
- **Malware Detection (if available)**
- **Under Credentials, add SSH or Windows credentials for a deeper scan.**
![image](https://github.com/user-attachments/assets/c7272c4d-fbf2-472c-b1a5-d9cdcbc4680a)
![image](https://github.com/user-attachments/assets/3504ad18-4c79-4377-b3e3-1d50fa127e18)
![image](https://github.com/user-attachments/assets/f4a54f51-4c02-42ba-a5fa-a0ca79f72948)
![image](https://github.com/user-attachments/assets/cf4fb748-3a18-4552-a688-5321b71443da)
![image](https://github.com/user-attachments/assets/a561b69b-4a03-42cd-94c5-4a73a56ff36d)
![image](https://github.com/user-attachments/assets/c2f977a6-47c0-4d88-b3be-f527367ba395)
![image](https://github.com/user-attachments/assets/6cf42cfe-2d17-4e77-af8d-82f1e51b14d7)
![image](https://github.com/user-attachments/assets/47fbc7e8-6640-4966-85a8-b1f8f98a36c5)
![image](https://github.com/user-attachments/assets/7556bbbe-dd41-46fd-acd0-c838361ffbf3)
![image](https://github.com/user-attachments/assets/a28b9da5-a8a1-4f02-8beb-6cd03e43073d)
![image](https://github.com/user-attachments/assets/b0ae13f8-07c8-4a62-9686-b9c7b92dd5c6)
![image](https://github.com/user-attachments/assets/892fad73-70b4-4bf5-8f9a-650896bad4b7)
![image](https://github.com/user-attachments/assets/bc9150b9-35fc-4240-92ac-8a015c34347f)
![image](https://github.com/user-attachments/assets/6ac5598a-c884-4256-b6c2-c0fb02a906d2)
![image](https://github.com/user-attachments/assets/69c0926d-d3e4-46d7-9d52-a21a0c4c1cf9)
![image](https://github.com/user-attachments/assets/9bbab199-d304-4177-8c5b-ffe670cbea2b)
![image](https://github.com/user-attachments/assets/497b9ffd-8906-4b11-96d3-fb1c20498884)

## Step 4: Web Application Scan (DVWA or OWASP BWA)

**Purpose: Identify web vulnerabilities such as SQL Injection, XSS, and authentication flaws.**

**Steps:Select New Scan → Web Application Tests.**
![image](https://github.com/user-attachments/assets/bc82243e-ee47-4673-bac8-2ad2c29aa86e)
![image](https://github.com/user-attachments/assets/2931c25a-1dcc-4ea9-acd5-a9659594c833)
![image](https://github.com/user-attachments/assets/1abd81da-3565-44d0-ae91-a2190700f871)
![image](https://github.com/user-attachments/assets/c531b370-1756-4326-9288-defbc2351d4a)
![image](https://github.com/user-attachments/assets/90eea1f0-8886-4fe4-a16e-70c489d2cd7e)
**Under Credentials, select HTTP Login Form:**
- **Username: admin**
- **Password: password**
- **Login URL: http://192.168.235.134/login.php**
![image](https://github.com/user-attachments/assets/5f226a1d-a132-4768-8567-a60b1bb48bfc)
**Click Save & Launch Scan.**
![image](https://github.com/user-attachments/assets/2cb74a17-3c85-46ed-a021-de2fbe211046)
![image](https://github.com/user-attachments/assets/c194fc32-28c2-412d-9e0c-0d1038954e65)
![image](https://github.com/user-attachments/assets/e9ff2bb3-93b3-4abe-a05c-105205c1cc07)
![image](https://github.com/user-attachments/assets/7a0c3389-d651-4ec4-b943-938b88c4a6a9)
![image](https://github.com/user-attachments/assets/185766df-c6ed-4936-9eca-db575043c0cf)

## Conclusion
**Through this Nessus-based vulnerability assessment project, I was able to:**

**Successfully perform Basic Network Scan , Host Discovery, Network Scanning, and Web Application Scanning in a controlled lab environment.**

**Identify critical, high, and medium-level vulnerabilities on test machines like Metasploitable 2 and DVWA.**

**Understand the importance of credentialed scans in uncovering deeper system weaknesses.**

**Learn how to properly configure scan policies, including advanced and custom settings for targeted assessments.**

**Gain hands-on experience in report generation, interpretation, and documentation of remediation steps.**

**This project not only strengthened my practical skills in using Nessus but also enhanced my ability to assess system security posture and recommend fixes. The experience will contribute significantly to my cybersecurity analyst portfolio and future job roles.**







