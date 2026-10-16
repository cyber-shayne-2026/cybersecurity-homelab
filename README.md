<h1> cybersecurity-homelab</h1>

 

<h2>Description</h2>
# Linux Server Hardening & SSH Security Demonstration

This is my first hands-on cybersecurity project. It demonstrates how to deploy, assess, and secure a Linux server environment using virtualization, network scanning, firewall configuration, and cryptographic authentication.

## 🚀 Project Overview
In this project, I configured an isolated virtual lab to simulate a real-world server deployment and defense scenario. I acted as both the security auditor (identifying vulnerabilities) and the systems administrator (hardening the infrastructure).

## 🛠️ Core Technologies & Tools
* **Hypervisor:** VirtualBox
* **Attacker/Auditor Machine:** Kali Linux
* **Target Environment:** Ubuntu Server
* **Network Security:** UFW (Uncomplicated Firewall)
* **Remote Management:** OpenSSH (Password vs. Key-Pair Authentication)
* **Reconnaissance:** Nmap (Network Mapper)

## 📑 Key Milestones & Demonstrations

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




<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://imgur.com/a/CdnL0Vd#nGiomYg" height="80%" width="80%" alt=/>
<br />
<br />

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
