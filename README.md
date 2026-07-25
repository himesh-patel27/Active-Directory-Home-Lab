# 🖧 Active Driectory Home Lab 

## 📌 Project Overview
This project involved designing and configuring a three-site enterprise network connected via point-to-point WAN links.  
Each site was assigned its own /26 subnet, and the WAN network was further subnetted into /30 networks for router-to-router connections.

## 🗂️ Tools Used

### 🌍 IP Addressing Scheme
- **Network Block:** `192.168.0.0/24`
- **LAN Subnets:**  
  - LAN 1: `192.168.0.64/26`  
  - LAN 2: `192.168.0.128/26`  
  - LAN 3: `192.168.0.192/26`  
- **WAN Subnets (/30):**  
  - WAN 1: `192.168.0.0/30`  
  - WAN 2: `192.168.0.4/30`  
  - WAN 3: `192.168.0.8/30`

### 🖥️ Device Setup
- **Routers:** 3 (PT-Empty) – connected in full mesh topology  
- **Switches:** 3 (PT-Empty) – one per site  
- **Access Points:** 3 (AP-PT-AC) – one per site  
- **Servers:** 3 – configured with DNS, DHCP, FTP, Email  
- **Printers:** 3 – static IP  
- **DHCP:** Configured per site to assign remaining IPs dynamically

### 🛠️ Configuration Steps
1. **Device Installation & Naming**  
   - Installed proper interfaces 
   - Labeled routers, switches, and end devices

2. **IP Addressing**  
   - Assigned **first valid IP** to each router interface
   - Assigned **second valid IP** to server, **third valid IP** to printer
   - Configured DHCP pools for each LAN

3. **Routing**  
   - Configured static routes between sites to ensure full connectivity

4. **Services Configuration**  
   - DNS, HTTPS, FTP, POP3, SMTP enabled on servers
   - Printers configured with static IPs
   - Wireless access points configured and tested

5. **Testing**  
   - Verified connectivity with **ping** and **traceroute**
   - Tested DHCP by checking client IP leases
   - Confirmed access to FTP, HTTP, and email services

## 🔑 Key Learnings
- Designed and implemented a multi-site network with subnetting and WAN links
- Practiced IP address planning and static route configuration
- Configured multiple network services (DNS, DHCP, FTP, Mail) in a lab environment
- Verified end-to-end connectivity and network functionality

## 📂 Files
- `final_proj-1.pka` – Main Packet Tracer file
- Screenshots – Proof of working network
