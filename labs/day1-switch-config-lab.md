# Day 1 – Basic Switch and Device Configuration Lab

This lab focuses on configuring basic device settings on switches and PCs using Cisco Packet Tracer.

---

## 🧪 Lab Objectives

- Set hostnames on switches
- Disable DNS lookup
- Set console and enable passwords
- Configure IP addresses on PCs
- Save configurations

---

## 🛠️ Devices Used

- 1 Cisco Switch
- 2 PCs

---

## 🔧 CLI Configuration Steps

```bash
# Set hostname and disable DNS lookup
enable
configure terminal
hostname Switch1
no ip domain-lookup

# Set console password
line console 0
password cisco
login
exit

# Set enable password
enable password class

# Save config
end
write memory
🖥️ PC IP Settings (Set manually via Packet Tracer GUI)
PC	IP Address	Subnet Mask	Default Gateway
PC1	192.168.1.10	255.255.255.0	192.168.1.1
PC2	192.168.1.11	255.255.255.0	192.168.1.1
✅ Expected Outcome
-> Switch displays configured hostname
-> Console and enable passwords prompt for login
-> PCs can ping each other if connected
🧠 Key Takeaways
->Basic switch CLI familiarity (hostname, passwords)
->CLI structure: exec mode → global config → line config
->Saving configs is critical (write memory or copy run start)
