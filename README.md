<h1> cybersecurity-homelab</h1>

 

<h2>Description</h2>
# Linux Server Hardening & SSH Security Demonstration

This is my first hands-on cybersecurity project. It demonstrates how to deploy, assess, and secure a Linux server environment using virtualization, network scanning, firewall configuration, and cryptographic authentication.

##  Project Overview
In this project, I configured an isolated virtual lab to simulate a real-world server deployment and defense scenario. I acted as both the security auditor (identifying vulnerabilities) and the systems administrator (hardening the infrastructure).

##  Core Technologies & Tools
* **Hypervisor:** VirtualBox
* **Attacker/Auditor Machine:** Kali Linux
* **Target Environment:** Ubuntu Server
* **Network Security:** UFW (Uncomplicated Firewall)
* **Remote Management:** OpenSSH (Password vs. Key-Pair Authentication)
* **Reconnaissance:** Nmap (Network Mapper)

##  Key Milestones & Demonstrations

### 1. Lab Environment Setup
* Deployed and configured **Kali Linux** and **Ubuntu Server** VMs within VirtualBox.
* Configured proper network adapter modes to ensure controlled communication between machines.

### 2. Vulnerability Assessment & Reconnaissance
* Conducted network scans from the Kali machine to map the Ubuntu server’s open ports and identify potential entry points.

### 3. Firewall Implementation (UFW)
* Safely configured and activated the **Uncomplicated Firewall (UFW)** on the Ubuntu server.
* Ensured persistent remote management capabilities by explicitly prioritizing and allowing SSH traffic before enabling the firewall rules.

### 4. Authentication Hardening: Passwords vs. SSH Keys
* **Phase 1:** Demonstrated standard password-based SSH authentication and analyzed its exposure to credential-guessing and brute-force attacks.
* **Phase 2:** Upgraded server security by generating an encrypted **Ed25519 SSH key pair** with a passphrase on Kali Linux.
* **Phase 3:** Successfully disabled password authentication server-wide, enforcing mandatory, multi-factor cryptographic key access.

<br />


##  Step-by-Step Lab Walkthrough

### Step 1: Conducting the Initial Vulnerability Scan
First, I utilized Nmap from the Kali Linux box to scan the target Ubuntu Server. This allowed me to see open ports and map out the target before applying security controls. I put the output into a file to save in case I need to look at this output again later. 
<img width="851" height="582" alt="VirtualBox_kali-linux-2026 1-virtualbox-amd64_15_10_2026_18_03_39" src="https://github.com/user-attachments/assets/7e65c890-0e1a-495c-a951-77e77d52efcc" />

<img width="851" height="501" alt="VirtualBox_kali-linux-2026 1-virtualbox-amd64_15_10_2026_18_09_27" src="https://github.com/user-attachments/assets/110bc500-4916-4a12-9850-5f15ad38aabe" />

---

### Step 2: Configuring the UFW Firewall Rules
To protect the server without losing administrative access, I explicitly allowed SSH traffic on Port 22 before enabling the firewall. I tested ssh just using a password first.
<img width="1280" height="558" alt="VirtualBox_ubuntu server_16_10_2026_10_19_59" src="https://github.com/user-attachments/assets/31b34459-cab0-4ccd-871c-78c8d462aa5a" />


<img width="877" height="518" alt="VirtualBox_kali-linux-2026 1-virtualbox-amd64_16_10_2026_10_21_51" src="https://github.com/user-attachments/assets/dd312945-7815-4c46-bf52-1628e9d7e696" />



---

### Step 3: Verifying Firewall Enforcement
After activating UFW, I verified that the ruleset was properly applied and active.
<img width="1280" height="270" alt="VirtualBox_ubuntu server_15_10_2026_18_36_01" src="https://github.com/user-attachments/assets/11b3883b-e679-4283-8496-926fb911ad1e" />




---

### Step 4: Testing Key-Based SSH Access
Finally, I verified that password authentication was successfully blocked and that the server would only accept the cryptographic Ed25519 key pair generated on Kali.
<img width="1280" height="756" alt="VirtualBox_ubuntu server_16_10_2026_10_31_23" src="https://github.com/user-attachments/assets/db6a06f4-78d1-41c8-832b-37724fc5403d" />

<img width="924" height="565" alt="VirtualBox_kali-linux-2026 1-virtualbox-amd64_16_10_2026_10_32_11" src="https://github.com/user-attachments/assets/8fd913a2-3088-4af0-b1e9-c756fee230ca" />





<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
