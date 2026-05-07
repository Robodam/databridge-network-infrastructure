# databridge-network-infrastructure
Secure SOHO Network Infrastructure project built using Cisco Packet Tracer. This project demonstrates LAN design, IP addressing, routing, inter-department communication, connectivity testing, troubleshooting, and basic ACL implementation for network security in a small business environment.
<!-- ========================================================= -->
<!--          SOHO NETWORK SECURITY PROJECT README             -->
<!-- ========================================================= -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=250&color=0:0f172a,100:00f7ff&text=SOHO%20Network%20Security%20Project&fontAlign=50&fontAlignY=40&fontSize=40&fontColor=ffffff&desc=Cisco%20Packet%20Tracer%20%7C%20Network%20Design%20%7C%20ACL%20Implementation&descAlignY=60"/>

# 🛡️ Building a Secure SOHO Network Infrastructure

### 🔐 Cisco Packet Tracer Network Design & Security Project

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=00F7FF&center=true&vCenter=true&width=900&lines=Secure+Network+Infrastructure;SOHO+Network+Design;Cisco+Packet+Tracer+Simulation;Routing+%26+ACL+Configuration;Network+Security+Implementation;Connectivity+Testing+%26+Troubleshooting"/>

</div>

---

# 📖 Project Overview

This project demonstrates the design and implementation of a **Secure Small Office/Home Office (SOHO) Network Infrastructure** using **Cisco Packet Tracer**.

The network was designed for a fictional company called:

# 🏢 DataBridge Innovations

The organization required a structured and secure internal network to support communication between its departments:

- 🗂️ Admin Department
- 💼 Sales Department
- 👥 HR Department

The project focused on:

✅ Network topology design  
✅ LAN setup and device configuration  
✅ IP addressing and subnetting  
✅ Inter-network communication  
✅ Connectivity testing and troubleshooting  
✅ Basic Access Control List (ACL) security implementation  

---

# 🎯 Project Objectives

✔️ Design a functional routed network  
✔️ Configure routers, switches, and end devices  
✔️ Implement proper IP addressing  
✔️ Enable secure communication between departments  
✔️ Simulate and test the network using Cisco Packet Tracer  
✔️ Apply basic ACL security policies  

---

# 🧠 Learning Outcomes

By completing this project, I gained hands-on experience in:

- 🛡️ Network Security Fundamentals
- 🌐 LAN Design & Implementation
- 🔀 Routing & Inter-network Communication
- 📡 IP Addressing & Subnetting
- ⚙️ Cisco Device Configuration
- 🧪 Connectivity Testing using Ping
- 🚨 Basic ACL Security Rules
- 🔍 Network Troubleshooting

---

# 🏗️ Network Topology

## 📌 Devices Used

| Device | Quantity |
|---|---|
| Cisco 2911 Router | 1 |
| Cisco 2960 Switch | 3 |
| PCs | 6 |
| Server | 1 |

---

# 🌐 Department Network Structure

| Department | Network/Subnet | Devices |
|---|---|---|
| 🗂️ Admin | 192.168.10.0/24 | 2 PCs & 1 Server |
| 💼 Sales | 192.168.20.0/24 | 2 PCs |
| 👥 HR | 192.168.30.0/24 | 2 PCs |

---

# 🖥️ Network Architecture

```text
                    ┌─────────────────┐
                    │   Cisco Router  │
                    │      2911       │
                    └────────┬────────┘
                             │
         ┌───────────────────┼───────────────────┐
         │                   │                   │

 ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
 │ Admin Switch │    │ Sales Switch │    │   HR Switch  │
 │    2960      │    │    2960      │    │    2960      │
 └──────┬───────┘    └──────┬───────┘    └──────┬───────┘
        │                   │                   │

   PCs & Server         Sales PCs            HR PCs
```

---

# ⚙️ IP Addressing Scheme

| Department | Router Gateway | Host Range |
|---|---|---|
| Admin | 192.168.10.1 | 192.168.10.10 - 192.168.10.11 |
| Sales | 192.168.20.1 | 192.168.20.10 - 192.168.20.11 |
| HR | 192.168.30.1 | 192.168.30.10 - 192.168.30.11 |

Subnet Mask for all networks:

```bash
255.255.255.0
```

---

# 🔧 Technologies & Tools Used

<div align="center">

<img src="https://skillicons.dev/icons?i=linux"/>

<br><br>

<img src="https://img.shields.io/badge/Cisco_Packet_Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white"/>

<img src="https://img.shields.io/badge/Networking-0A66C2?style=for-the-badge"/>

<img src="https://img.shields.io/badge/Network_Security-111827?style=for-the-badge"/>

<img src="https://img.shields.io/badge/ACL_Configuration-DC2626?style=for-the-badge"/>

<img src="https://img.shields.io/badge/Routing-2563EB?style=for-the-badge"/>

<img src="https://img.shields.io/badge/IP_Addressing-059669?style=for-the-badge"/>

</div>

---

# 🚀 Project Workflow

## 🥇 Step 1 — Network Setup

- Added:
  - 1 Cisco 2911 Router
  - 3 Cisco 2960 Switches
  - 6 PCs
  - 1 Server
- Connected devices using straight-through cables

---

## 🥈 Step 2 — Device Configuration

Configured:

- Router interfaces
- PC IP addresses
- Default gateways
- Basic switch connectivity

---

## 🥉 Step 3 — Connectivity Testing

Performed:

- Ping tests between departments
- Verification of inter-network communication
- Troubleshooting of failed connections

---

# 🔐 ACL Security Configuration

## 🎯 Security Requirement

The HR department should:

❌ NOT be able to ping the Admin Department

While:

✅ All other traffic remains allowed

---

# 🛡️ ACL Configuration Example

```bash
access-list 101 deny icmp 192.168.30.0 0.0.0.255 192.168.10.0 0.0.0.255
access-list 101 permit ip any any

interface g0/0
ip access-group 101 in
```

---

# ✅ Connectivity Test Results

| Test | Result |
|---|---|
| Sales ➜ Admin | ✅ Successful |
| Admin ➜ HR | ✅ Successful |
| HR ➜ Admin | ❌ Blocked by ACL |
| HR ➜ Sales | ✅ Successful |

---

# 📸 Project Screenshots

## 🖼️ Add Screenshots Here

You can include:

- Network topology screenshots
- Successful ping tests
- Failed ACL ping tests
- Router configuration screenshots
- Cisco Packet Tracer workspace

Example:

```markdown
![Topology](images/topology.png)
```

---

# 📂 Repository Structure

```bash
📦 soho-network-security-cisco-packet-tracer
 ┣ 📂 screenshots
 ┣ 📜 README.md
 ┣ 📜 network-topology.pkt
 ┣ 📜 acl-configuration.txt
 ┗ 📜 project-report.pdf
```

---

# 🏢 Business Impact

This project helps demonstrate how a properly designed network can:

✅ Improve communication efficiency  
✅ Enhance network organization  
✅ Increase reliability and scalability  
✅ Improve troubleshooting processes  
✅ Strengthen internal network security  

---

# 🎓 Accreditation

### DATA BRIDGE INNOVATIONS

Accredited by the:

## 🏛️ American Council of Training and Development

---

# 👨‍💻 Author

## Damilola Adeniye

### Cybersecurity Professional | Network Security Enthusiast

<div align="center">

<a href="https://linkedin.com/in/YOUR_LINKEDIN">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>

<a href="https://github.com/YOUR_GITHUB_USERNAME">
  <img src="https://img.shields.io/badge/GitHub-121011?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<a href="mailto:YOUR_EMAIL@gmail.com">
  <img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>

<a href="https://drive.google.com/YOUR_CV_LINK">
  <img src="https://img.shields.io/badge/Download_CV-FF0000?style=for-the-badge&logo=adobeacrobatreader&logoColor=white"/>
</a>

</div>

---

# ⭐ Project Highlights

```yaml
Project Type: Secure SOHO Network Infrastructure
Environment: Cisco Packet Tracer
Security Feature: Access Control List (ACL)
Network Type: Routed LAN
Focus Areas:
  - Networking
  - Routing
  - Network Security
  - Troubleshooting
  - ACL Configuration
```

---

<div align="center">

# 🔐 “A secure network is the foundation of a secure business.”

⭐ If you found this project useful, feel free to star the repository!

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&height=120&section=footer&color=0:0f172a,100:00f7ff"/>
