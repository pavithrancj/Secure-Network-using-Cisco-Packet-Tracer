# Network Configuration Project: Multi-Zone Network with Cisco ASA Firewall

## 🖧 Overview  
This project involves designing and implementing a segmented network consisting of three security zones—Inside, DMZ, and Outside—using Cisco Packet Tracer and a Cisco ASA 5506 firewall. The goal was to ensure secure communication between zones while enforcing strict access control and NAT policies.

---

## 🎯 Objectives  
- Design a secure network topology with multiple zones  
- Assign static IP addressing consistent with each zone subnet  
- Configure firewall interfaces with appropriate security levels  
- Implement ACLs to control HTTP, HTTPS, and ICMP traffic  
- Enable secure web server access via HTTPS in the DMZ  
- Create an exceptional firewall rule allowing limited external access  
- Test and verify connectivity and access control  

---

## 🛠️ Devices and Zones  

| Zone       | IP Range          | Devices                    |
|------------|-------------------|----------------------------|
| Inside     | 192.168.20.0/24   | PC0, PC1                   |
| DMZ        | 172.16.20.0/28    | Web Server 1, Web Server 2 |
| Outside    | 110.20.20.0/29    | PC3                        |

---

## 🔧 Key Configuration Details

### Firewall Interfaces  
- **Inside (GigabitEthernet0/1):** 192.168.20.1 /24, security-level 100  
- **DMZ (GigabitEthernet0/2):** 172.16.20.1 /28, security-level 50  
- **Outside (GigabitEthernet0/3):** 110.20.20.1 /29, security-level 0  

### ACL Highlights  
- Allowed HTTP (port 80) and HTTPS (port 443) from Inside zone to DMZ web servers  
- Permitted ICMP (ping) traffic to and from web servers for troubleshooting  
- Created specific rules for external PC3 to access Web Server 1 on HTTP/HTTPS  

### NAT Configuration  
- Dynamic NAT for Inside and DMZ subnets mapped to Outside interface  

---

## ✅ Testing and Verification  
- PCs inside the network successfully ping and browse DMZ web servers  
- External PC3 access to Web Server 1 allowed as per firewall exception  
- HTTPS traffic properly handled, ensuring secure web server communication  
- ICMP inspection enabled to allow ping replies across zones  

---

> For full configuration details, commands, diagrams, and test results, please refer to the complete project report here:  
> 📄 [Full Network Configuration Project Report](https://github.com/pavithrancj/Secure-Network-using-Cisco-Packet-Tracer/blob/main/Network%20Configuration.pdf)  
