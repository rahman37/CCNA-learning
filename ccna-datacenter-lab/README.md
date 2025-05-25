# Enterprise Data Center Simulation (CCNA Lab)

This project simulates a scalable, enterprise-grade Layer 2/3 data center network using Cisco Packet Tracer. It includes VLAN segmentation, inter-VLAN routing via Router-on-a-Stick, DHCP, trunking, SSH security, and more — aligning with CCNA-level objectives.


DC.png


## 📌 Project Objectives

- Design a 3-tier enterprise network topology (Core, Distribution, Access)
- Implement VLANs for user and management segmentation
- Configure inter-VLAN routing using sub-interfaces
- Automate IP assignment via DHCP
- Secure switch access using SSH
- Practice trunking, access ports, EtherChannel (optional), and ACLs

---

## 🧱 Topology Overview

| Layer         | Devices        | Role                                      |
|---------------|----------------|-------------------------------------------|
| Core          | 1 Router       | Routing between VLANs, DHCP server        |
| Distribution  | 2 Switches     | Trunking, redundancy, Layer 2 forwarding  |
| Access        | 2 Switches     | PC connectivity, VLAN segmentation        |

---

## 🧩 VLANs and IP Schema

| VLAN  | Purpose         | Subnet             | Devices         |
|--------|------------------|----------------------|-----------------|
| 10     | User PCs         | 192.168.10.0/24      | PC2–PC4, PC6–PC8 |
| 99     | Management VLAN  | 192.168.99.0/24      | PC1, PC5, all switches (SVIs) |

---

## 🔐 Security Features

- SSH configured on all switches with local authentication
- Telnet access disabled (`transport input ssh`)
- Optional ACLs can restrict VTY access to VLAN 99 subnet

---

## ⚙️ Technologies Used

- Cisco Packet Tracer
- VLANs, Trunking, Router-on-a-Stick
- DHCP, ACLs (optional)
- SSH, Port Security (optional)

---

## 📁 Repository Structure

