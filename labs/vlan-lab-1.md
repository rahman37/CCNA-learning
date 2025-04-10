# VLAN Lab 1 – Basic VLAN Configuration

This lab covers the basics of VLAN creation and assigning ports to VLANs on a Cisco switch.

---

## 🧪 Lab Objective

- Create two VLANs: VLAN 10 (HR) and VLAN 20 (IT)  
- Assign 2 switch ports to each VLAN  
- Verify VLAN setup and connectivity

---

## 🛠️ Devices Used

- 1 Cisco Switch (2960 or similar)
- 4 PCs (connected to switch ports Fa0/1 to Fa0/4)

---

## 🧱 Network Setup

| Device | Port      | VLAN | Function |
|--------|-----------|------|----------|
| PC1    | Fa0/1     | 10   | HR       |
| PC2    | Fa0/2     | 10   | HR       |
| PC3    | Fa0/3     | 20   | IT       |
| PC4    | Fa0/4     | 20   | IT       |

---

## 🔧 CLI Commands Used

```bash
enable
configure terminal

# Create VLANs
vlan 10
name HR
vlan 20
name IT

# Assign ports to VLANs
interface range Fa0/1 - 2
switchport mode access
switchport access vlan 10

interface range Fa0/3 - 4
switchport mode access
switchport access vlan 20

# Verify VLAN assignment
end
show vlan brief
✅ Expected Outcome
PC1 and PC2 (VLAN 10) can ping each other

PC3 and PC4 (VLAN 20) can ping each other

Devices in different VLANs cannot ping each other without routing (Layer 3)

🧠 Key Learning Points
VLANs segment traffic even within the same physical switch

Access ports can only belong to one VLAN

Use show vlan brief to confirm config
