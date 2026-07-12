# AD-lab

## Objective

Built a Windows Server 2022 Active Directory environment to simulate a small enterprise network. Configured a Domain Controller, DNS, DHCP, and RRAS/NAT services, then deployed a Windows 10 client joined to the domain. Automated the creation of over 1,000 Active Directory user accounts using PowerShell.

### Skills Learned

- Active Directory Domain Services (AD DS)
- Windows Server Administration
- Active Directory Users and Computers (ADUC)
- DHCP Configuration
- DNS Configuration
- RRAS / NAT
- Domain Management
- PowerShell Automation
- Virtual Machine Administration
- Windows 10 Domain Join
- Network Troubleshooting

### Tools Used

- Windows Server 2022
- Windows 10 Pro
- VirtualBox
- PowerShell
- Active Directory
- DHCP
- DNS
- RRAS
- GitHub
  
## Steps

1. Created Virtual Machines
Installed Windows Server 2022
Installed Windows 10 Pro
Configured networking in VirtualBox
NAT Adapter for Internet connectivity
Internal Network adapter for private domain communication

2. Configured Domain Controller
Renamed server to DC
Assigned static IP address

IP Address:
172.16.0.1
Subnet Mask:
255.255.255.0
DNS:
127.0.0.1

<img width="585" height="142" alt="image" src="https://github.com/user-attachments/assets/411807a1-7a4b-4fea-9c2a-f63ec49caef8" />

3. Installed Active Directory
Installed:
Active Directory Domain Services (AD DS)
Promoted the server to a Domain Controller, naming the forest "mydomain.com"

4. Configured RRAS
Installed:
Remote Access Routing
Configured:
NAT
Internet sharing for internal clients
Result:
Windows 10 clients on the internal network gained Internet access while remaining joined to the private domain.

5.Configured DHCP
Installed DHCP Server role.
Created an IPv4 scope.

<img width="591" height="387" alt="image" src="https://github.com/user-attachments/assets/7237f154-1b35-4cfa-bdaf-450ca1bca2df" />

Gateway:
172.16.0.1
Authorized DHCP within Active Directory.

Added Windows 10 Client
Configured:
Internal Network Adapter
Joined the client computer to:

<img width="411" height="426" alt="image" src="https://github.com/user-attachments/assets/d0efca03-0854-40b4-a807-06c988aae461" />

Automated User Creation
Downloaded a PowerShell script containing sample user data from IT profesional, Josh Madaokor's github.
Executed the script using PowerShell ISE as Administrator.

<img width="612" height="426" alt="image" src="https://github.com/user-attachments/assets/5b770bc5-aecc-43cb-8a5d-512d1b82de26" />
