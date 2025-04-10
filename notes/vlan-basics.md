# VLAN Basics – Notes

**VLAN** stands for **Virtual Local Area Network**. It allows a single switch to be logically segmented into multiple networks, increasing security and reducing broadcast domains.

---

## 📌 Why VLANs?

- Separate network traffic logically (without needing multiple switches)
- Improve **security** and **broadcast control**
- Group users by function, not location (e.g., HR, Sales, IT)

---

## 🎨 VLAN ID Ranges

- **Standard Range:** 1 – 1005  
- **Extended Range:** 1006 – 4094  
- Reserved VLANs:
  - VLAN 1 → Default VLAN (used for control traffic like CDP)
  - VLAN 1002–1005 → Reserved for legacy use (FDDI, Token Ring)

---

## 🔧 Key Cisco CLI Commands

```bash
# Enter global configuration
configure terminal

# Create VLAN 10
vlan 10

# Name the VLAN (optional)
name HR

# Assign a port to VLAN 10
interface FastEthernet0/1
switchport mode access
switchport access vlan 10
🌐 Types of VLAN Ports
Port Type	Description
Access Port	Belongs to one VLAN only
Trunk Port	Carries multiple VLANs using tags
Trunking Protocols:

802.1Q → industry standard

ISL (legacy Cisco)

🧠 Quick Facts
VLANs reduce the size of broadcast domains

Devices in different VLANs cannot communicate without a router or Layer 3 switch

Trunk ports use VLAN tags to identify traffic

🧪 Practice Command
bash
Copy
Edit
show vlan brief
Displays all VLANs configured on a switch.

bash
Copy
Edit
show interfaces trunk
Lists interfaces operating as trunk ports.
