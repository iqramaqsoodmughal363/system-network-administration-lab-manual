<!--
╔══════════════════════════════════════════════════════════════════╗
║  ███████╗██╗   ██╗███████╗████████╗███████╗███╗   ███╗        ║
║  ██╔════╝╚██╗ ██╔╝██╔════╝╚══██╔══╝██╔════╝████╗ ████║        ║
║  ███████╗ ╚████╔╝ ███████╗   ██║   █████╗  ██╔████╔██║        ║
║  ╚════██║  ╚██╔╝  ╚════██║   ██║   ██╔══╝  ██║╚██╔╝██║        ║
║  ███████║   ██║   ███████║   ██║   ███████╗██║ ╚═╝ ██║        ║
║  ╚══════╝   ╚═╝   ╚══════╝   ╚═╝   ╚══════╝╚═╝     ╚═╝        ║
╚══════════════════════════════════════════════════════════════════╝
-->

<div align="center">

# 🖥️ SYSTEM & NETWORK ADMINISTRATION
# LAB MANUAL (DI-323L)

> *"Master the art of managing systems, networks, and infrastructure."*

[![Made with ❤️](https://img.shields.io/badge/Made%20with-❤️-red.svg)](https://github.com/iqramaaqsoodmughal363)
[![Course](https://img.shields.io/badge/Course-DI--323L-blue.svg)](https://github.com/iqramaaqsoodmughal363)
[![University](https://img.shields.io/badge/University-Punjab%20University-800080.svg)](https://github.com/iqramaaqsoodmughal363)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen.svg)](https://github.com/iqramaaqsoodmughal363)

</div>

---

## 📋 Overview

<div align="center">
<table>
<tr>
<td width="50%">
<b>🎯 WHAT'S INSIDE</b><br><br>
🔹 Server Environment & OS Setup<br>
🔹 Linux Boot & Process Management<br>
🔹 IPTables Firewall Configuration<br>
🔹 Bash Scripting Automation<br>
🔹 NFS, Samba & FTP Servers<br>
🔹 DNS, DHCP & Apache Web Server<br>
🔹 Windows Server & Active Directory<br>
🔹 VLAN, Trunking & Switching<br>
🔹 Routing (Static, RIP)<br>
🔹 Access Control Lists (ACL)
</td>
<td width="50%">
<b>⚡ QUICK STATS</b><br><br>
📚 <b>10</b> Comprehensive Chapters<br>
💻 <b>50+</b> Commands & Configs<br>
🎓 <b>20</b> Viva Questions with Answers<br>
🛠️ <b>Linux</b> + <b>Windows</b> + <b>Cisco</b><br>
📖 Complete Lab Manual in HTML<br>
✅ Step-by-Step Execution Guides
</td>
</tr>
</table>
</div>

---

## 🎨 Chapter Preview

<div align="center">

| # | Chapter | 🔥 Key Topics |
|:-:|:---|:---|
| 1 | **Server Environment & OS Setup** | Static IP, Netplan, Network Verification |
| 2 | **Linux Boot & Process Control** | Systemd, Kill, Nice, Top, Process States |
| 3 | **IPTables Firewall** | Filter, NAT, Mangle, ACCEPT/DROP/REJECT |
| 4 | **Bash Scripting** | Automation, Logging, Cron, Shebang |
| 5 | **NFS, Samba & FTP** | Cross-platform File Sharing |
| 6 | **DNS, DHCP & Apache** | Core Network Services |
| 7 | **Windows Server & AD** | Active Directory, Users, Groups, OU |
| 8 | **VLAN & Trunking** | 802.1Q, Access/Trunk Ports |
| 9 | **Routing (Static, RIP)** | Hop Count, Routing Tables |
| 10 | **Access Control Lists** | Standard & Extended ACLs |

</div>

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone https://github.com/iqramaaqsoodmughal363/system-network-administration-lab-manual.git

# Open the lab manual in your browser
open Lab_Manual.html
```

---

## 💻 Command Cheatsheet

### 🔷 Linux Network Configuration

```bash
ip a                              # Show network interfaces
sudo nano /etc/netplan/01-netcfg.yaml  # Edit static IP
sudo netplan apply                # Apply network changes
ping -c 4 192.168.1.1             # Test connectivity
```

### 🔷 Process Management

```bash
systemctl get-default             # Show boot target
sudo systemctl set-default multi-user.target  # Set CLI mode
ps aux | grep apache2             # Search process
kill -9 PID                       # Force kill
top                               # Real-time monitoring
```

### 🔷 IPTables Firewall

```bash
sudo iptables -F                  # Clear all rules
sudo iptables -P INPUT DROP       # Default policy (block incoming)
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT  # Allow SSH
sudo iptables -L -v -n            # List all rules
```

### 🔷 Bash Scripting

```bash
nano sys_monitor.sh               # Create script
chmod +x sys_monitor.sh           # Make executable
./sys_monitor.sh                  # Run script
cat /var/log/sys_audit.log        # View log
```

### 🔷 File Sharing (NFS / Samba)

```bash
sudo mkdir -p /srv/nfs_share      # Create NFS share
sudo nano /etc/exports            # Edit NFS exports
sudo exportfs -a                  # Apply NFS changes
sudo smbpasswd -a username        # Add Samba user
sudo systemctl restart smbd       # Restart Samba
```

### 🔷 DNS / DHCP / Apache

```bash
sudo nano /etc/dhcp/dhcpd.conf    # Edit DHCP config
sudo systemctl restart isc-dhcp-server  # Restart DHCP
sudo nano /etc/bind/db.enterprise.local  # Edit DNS zone
sudo a2ensite enterprise.conf     # Enable Apache site
sudo systemctl reload apache2     # Reload Apache
```

### 🔷 Windows Server (PowerShell)

```powershell
Install-WindowsFeature -Name AD-Domain-Services
Install-ADDSForest -DomainName "enterprise.local"
New-ADOrganizationalUnit -Name "IT_Dept"
New-ADUser -Name "JohnDoe" -SamAccountName "jdoe"
Add-ADGroupMember -Identity "IT_Admins" -Members "jdoe"
```

### 🔷 Cisco Switch / Router

```bash
enable                            # Privileged mode
configure terminal                # Global config
hostname SW-CORE-01               # Set hostname
vlan 10                           # Create VLAN
switchport mode trunk             # Set trunk mode
ip route 192.168.20.0 255.255.255.0 10.0.0.2  # Static route
router rip                        # Enable RIP
access-list 10 deny host 192.168.1.50  # Standard ACL
ip access-group 10 out            # Apply ACL
```

---

## 🎓 Viva Questions (20 Qs with Answers)

<details>
<summary><b>📌 Click to Expand Viva Questions</b></summary>

| # | Question | Answer |
|:-:|:---|:---|
| 1 | Why do servers require static IP addresses? | Servers provide continuous network services. Dynamic IP changes break client requests, DNS records, and active connections. |
| 2 | What is the purpose of Swap partition? | Swap serves as secondary memory on hard disk space when physical RAM is completely filled. |
| 3 | What is a Zombie Process? | A process that has completed execution but its entry remains in the process table because its parent process hasn't read its exit status. |
| 4 | What is the highest priority nice value in Linux? | -20 is the highest priority, while +19 is the lowest priority. |
| 5 | Difference between DROP and REJECT in IPTables? | DROP silently discards packets. REJECT drops and returns an ICMP error. |
| 6 | Which table handles NAT in IPTables? | The NAT table, using PREROUTING and POSTROUTING chains. |
| 7 | What is the purpose of the Shebang (`#!/bin/bash`) line? | It specifies the absolute interpreter path required to execute the commands within the script. |
| 8 | Which protocol enables Linux to share files with Windows OS? | Samba (using the SMB/CIFS protocol). |
| 9 | Difference between NFS and Samba? | NFS is optimized for Unix/Linux; Samba provides cross-platform file/print sharing with AD integration. |
| 10 | Explain the DHCP DORA process. | Discover (client broadcast), Offer (server response), Request (client selection), Acknowledge (server confirms lease). |
| 11 | What is the purpose of a DNS PTR record? | PTR records map an IP address to a Domain Name (Reverse DNS Lookup). |
| 12 | Difference between Group and Organizational Unit (OU)? | OU is a container for delegation and GPOs. Group is used to grant access permissions. |
| 13 | What is the FSMO role in AD DS? | Flexible Single Master Operations roles assigned to specific DCs to prevent database update conflicts. |
| 14 | What framing standard is used for Trunk links? | IEEE 802.1Q standard, which inserts a 4-byte VLAN tag into Ethernet frames. |
| 15 | Can hosts on VLAN 10 talk to VLAN 20 directly on a Layer 2 switch? | No, traffic between VLANs requires a Layer 3 device (Router or Layer 3 Switch). |
| 16 | What is the maximum hop count for RIP protocol? | Maximum hop count is 15. A hop count of 16 indicates unreachable. |
| 17 | What metric does RIP use to select the best path? | Hop Count (number of routers traversed). |
| 18 | Where should Standard ACLs be placed? | As close to the destination network as possible. |
| 19 | What is the implicit rule at the end of every ACL? | An invisible `deny ip any any` rule that blocks all unmatched traffic. |
| 20 | What is the difference between Standard and Extended ACLs? | Standard ACLs filter by Source IP only. Extended ACLs filter by Source IP, Destination IP, Protocol, and Port. |

</details>

---

## 🛠️ Tools & Technologies Covered

<div align="center">

| **Category** | **Tools** |
|:---|:---|
| **Linux** | Ubuntu Server, Netplan, Systemd, IPTables, Bash |
| **Windows** | Windows Server, Active Directory, PowerShell |
| **Cisco** | IOS, VLAN, Trunking, Static Routing, RIP, ACL |
| **Services** | NFS, Samba, FTP, DNS, DHCP, Apache |
| **Protocols** | TCP/IP, ICMP, ARP, DNS, DHCP, HTTP, SSH, SMB |

</div>

---

## 📂 File Structure

```
system-network-administration-lab-manual/
│
├── 📄 Lab_Manual.html      # Complete lab manual (HTML)
└── 📄 README.md            # This file
```

---

## 👩‍💻 Author

<div align="center">

### **Iqra Maqsood Mughal**

*Software Engineer · Full-Stack Developer · Code Craftsman · Android App Developer · Problem Solver* 🚀

```js
const 💻 = "Code is life";
while (true) { learn(); build(); innovate(); }
```

</div>

---

## 📅 Date

**September 7, 2026**

---

## 📄 License

<div align="center">

This lab manual is intended for **educational and personal study purposes**.

</div>
