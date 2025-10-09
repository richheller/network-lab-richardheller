# Active Directory Setup

This lab demonstrates the configuration of **Active Directory Domain Services (AD DS)** within my LoonsLabUSA network sandbox. 
The environment is designed to simulate a small enterprise domain integrated with my Cisco network infrastructure.

---

## 🧠 Objective
Deploy a Windows Server 2022 domain controller for centralized authentication, DNS/DHCP, and Group Policy management.

---

## 🧩 Domain Information
- **Domain Name:** LoonsLabUSA.local 
- **Server:** Boulder-DC01 
- **Operating System:** Windows Server 2022 Datacenter (VirtualBox) 
- **Integrated Services:** AD DS, DNS, DHCP

---

## 🗂️ Organizational Units
The OU structure reflects geographic regions and themed user groups used for testing Group Policy Objects and authentication scenarios.

| OU | Example Users | Notes |
|----|----------------|-------|
| Boulder | Axel_Foley, Victor_Maitland | Default DC, initial test users |
| Denver | Rocky_Balboa, Apollo_Creed | OSPF Area 0 VLAN integration |
| LosAngeles | Rick_Dalton, Cliff_Booth | Used for GPO login scripts |
| NewYork | Snake_Plissken, Brain, Maggie | Secondary domain test set |

---

## 👥 Users
Below is a snapshot of configured users and OUs inside **Active Directory Users and Computers**:

![Active Directory Users](./screenshots/ad-users.png)

---

## 🔧 Next Steps
- Add Group Policy objects to enforce login scripts and wallpapers 
- Integrate DNS zones with Cisco VLAN 50 (“Loons_Lab”) 
- Enable DHCP scope management and DNS dynamic updates


<img width="1052" height="727" alt="{EFA0A82A-9EBD-44AA-A7B1-38D25FC75487}" src="https://github.com/user-attachments/assets/cd83dd7c-5a48-4dc5-8713-9767b06fded6" />
