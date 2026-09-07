# 🖥️ System & Network Administration Lab Manual (DI-323L)

> Complete System & Network Administration Lab Manual covering Linux, Windows Server, Cisco networking, and security.

---

## 📋 Overview

This lab manual is designed for the **System & Network Administration (DI-323L)** course affiliated with Punjab University. It provides step-by-step command execution guides, theory explanations, and viva questions for each chapter.

**Topics Covered:**
- Server Environment & OS Setup
- Linux Boot Management, Process Control & Monitoring
- Packet Filtering & Network Traffic Security (IPTables)
- Automation — Bash Scripting
- Network File Servers (NFS, Samba, FTP)
- Core Network Services (DNS, DHCP, Apache)
- Windows Server Administration & Active Directory DS
- Managed Switches, Access Points & VLAN Trunking
- WAN Networking & Routing Protocols (Static, RIP)
- Router Security — Access Control Lists (Standard & Extended)

---

## 📂 File Included
system-network-administration-lab-manual/
│
├── Lab_Manual.html # Complete lab manual in HTML format
└── README.md # This file

text

---

## 📚 Chapter Breakdown

| Chapter | Topic |
| :---: | :--- |
| 1 | Foundation — Server Environment & OS Setup |
| 2 | Linux Boot Management, Process Control & Monitoring |
| 3 | Packet Filtering & Network Traffic Security (IPTables) |
| 4 | Automation — Bash Scripting |
| 5 | Infrastructure Sharing — NFS, Samba, FTP |
| 6 | Core Network Services — DNS, DHCP & Apache |
| 7 | Windows Server Administration & Active Directory DS |
| 8 | Managed Switches, Access Points & VLAN Trunking |
| 9 | WAN Networking & Routing Protocols (Static, RIP) |
| 10 | Router Security — Access Control Lists (ACL) |

---

## 🛠️ How to Use

1. Open the HTML file in your browser
2. Navigate to the desired chapter
3. Follow the step-by-step command execution guides
4. Review the viva questions for exam preparation
5. Use the commands as reference for lab work

---

## 🧠 Key Commands Summary

### Network Configuration (Ubuntu)
```bash
ip a                           # Show network interfaces
sudo nano /etc/netplan/01-netcfg.yaml  # Edit static IP
sudo netplan apply             # Apply network changes
ping -c 4 192.168.1.1          # Test connectivity
Process Management
bash
systemctl get-default          # Show boot target
sudo systemctl set-default multi-user.target  # Set CLI mode
ps aux | grep apache2          # Search process
kill -9 PID                    # Force kill process
top                            # Real-time system monitoring
Firewall (IPTables)
bash
sudo iptables -F               # Clear all rules
sudo iptables -P INPUT DROP    # Default policy (block incoming)
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT  # Allow SSH
sudo iptables -L -v -n         # List all rules
Bash Scripting
bash
nano sys_monitor.sh            # Create script
chmod +x sys_monitor.sh        # Make executable
./sys_monitor.sh               # Run script
cat /var/log/sys_audit.log     # View log
File Sharing
bash
sudo mkdir -p /srv/nfs_share   # Create NFS share
sudo nano /etc/exports         # Edit NFS exports
sudo exportfs -a               # Apply NFS changes
sudo smbpasswd -a username     # Add Samba user
sudo systemctl restart smbd    # Restart Samba
DNS / DHCP / Apache
bash
sudo nano /etc/dhcp/dhcpd.conf # Edit DHCP config
sudo systemctl restart isc-dhcp-server  # Restart DHCP
sudo nano /etc/bind/db.enterprise.local  # Edit DNS zone
sudo a2ensite enterprise.conf  # Enable Apache site
sudo systemctl reload apache2  # Reload Apache
Windows Server (PowerShell)
powershell
Install-WindowsFeature -Name AD-Domain-Services  # Install AD
Install-ADDSForest -DomainName "enterprise.local"  # Create forest
New-ADOrganizationalUnit -Name "IT_Dept" -Path "DC=enterprise,DC=local"
New-ADUser -Name "JohnDoe" -SamAccountName "jdoe" ...
Add-ADGroupMember -Identity "IT_Admins" -Members "jdoe"
Cisco Switch / Router (CLI)
bash
enable                         # Enter privileged mode
configure terminal             # Enter global config
hostname SW-CORE-01            # Set hostname
vlan 10                        # Create VLAN
interface range fastEthernet 0/1 - 5  # Select ports
switchport mode trunk          # Set trunk mode
ip route 192.168.20.0 255.255.255.0 10.0.0.2  # Static route
router rip                     # Enable RIP
access-list 10 deny host 192.168.1.50  # Standard ACL
ip access-group 10 out         # Apply ACL
📊 Quick Reference Table
Tool / Service	Command to Start	Config File
SSH	sudo systemctl start ssh	/etc/ssh/sshd_config
Apache	sudo systemctl start apache2	/etc/apache2/sites-available/
DHCP	sudo systemctl start isc-dhcp-server	/etc/dhcp/dhcpd.conf
DNS (BIND)	sudo systemctl start bind9	/etc/bind/named.conf
NFS	sudo systemctl start nfs-kernel-server	/etc/exports
Samba	sudo systemctl start smbd	/etc/samba/smb.conf
🎯 Viva Questions Included
Every chapter includes 2 viva questions with answers for exam preparation:

Chapter	Sample Viva Q
1	Why do servers require static IP addresses?
2	What is a Zombie Process?
3	Difference between DROP and REJECT in IPTables?
4	What is the purpose of the Shebang (#!/bin/bash) line?
5	Difference between NFS and Samba?
6	Explain the DHCP DORA process.
7	Difference between Group and Organizational Unit (OU)?
8	What framing standard is used for Trunk links?
9	What is the maximum hop count for RIP protocol?
10	Where should Standard ACLs be placed?
👩‍💻 Author
Iqra Maqsood Mughal
Software Engineer | Full-Stack Developer | Code Craftsman | Android App Developer | Problem Solver 🚀

js
const 💻 = "Code is life";
while (true) { learn(); build(); innovate(); }
📅 Date
September 7, 2026

📄 License
This lab manual is intended for educational and personal study purposes.
