# AD-lab

## Objective

I wanted to build an active directory lab in order to gain expience in a real world environment with many clients. 

### Skills Learned

- how to set up an active directory server
- networking
- 

### Tools Used

- VirtualBox
  
## Steps

Don't install guest additions until windows installed fully- will mess up boot

Use desktop experience version

Admin- Password1

Allow connection to other devices 

Devices- insert guest additions cd

Go to files- find guest additions amd64 
Then install that then shutdown 

Rename networks based on ip addresses 
10…. Is the home router connection
The automatic one is the internal

Change name of pc to DC by right clicking windows button -system then restart 

Change ip address (172.16.0.1)+ subnet mask(255.255.255.0+ no default gateway + dns for internal connection (127.0.0.1)

Add roles and features through server manager 
Click next> next> select server> choose active directory domain services> add features> next until install 
Then click flag to promote to domain > add new forest> mydomain.com > same password > uncheck dns delegation > next until install (will restart) 

Windows button> admin> users and computers 
Create new organizational unit by right clicking mydomain.com called _admins
Then add new user to that -my name
Make myself member of “domain admins”for object name then ok until it is underlined then okay >apply

Sign out 
Then login into other admin user> a-cblunt + password 

RAS/NAT for network connection for windows client

Roles and features again then check remote acces for roles> next until routing check  > then next until install 

Then go to tools > routing and remote access> DC(local) right click configure and enable > then next until choose NAT for external client connection through 1 IP 
Using 2022 version may be issue with RAS/NAT

Add tools- dhcp>tools > DHCP create new scope for ipv4
Name 172.16.0.100-200
Start …100
end  …200
length - 24
subnetmask - 255.255.255.0
Want to configure DHCP option 
Ip address which has nat configured 

Make sure server is up and running when opening client windows machine 
Chance pc name(advanced) to client1 and domain to mydomain.com 

Make sure client ip addresses are set to automatic 

Download zip file from joshmadakor AD_PS github 

Extract then open windows powershell ISE as admin
Open script 1_Create_users.ps1
Need to Set-ExecutionPolicy Unrestricted 
Then yes to all 
Then cd to  names.txt location 

When client gets address will shows in servers dhcp address leases

Since in domain any client can login 

Example below

<img width="596" height="400" alt="Screenshot 2025-12-22 163016" src="https://github.com/user-attachments/assets/a5b856c0-4063-4c39-858c-623c8fff7fcc" />


*Ref 1: vulnerability scan*
