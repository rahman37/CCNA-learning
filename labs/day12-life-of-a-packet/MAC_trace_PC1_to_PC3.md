# MAC Address Flow: PC1 to PC3 (Same LAN)

## 🧭 Scenario
PC1 and PC3 are on the same subnet: `192.168.1.0/24`. This means the packet never leaves the local LAN and no router is involved. The destination MAC is resolved via ARP before sending the ICMP packet.

---

## 🔹 A. PC1 → SW1
- **Source MAC:** `aaaa` (MAC of PC1’s FastEthernet0/1)
- **Destination MAC:** `3333` (MAC of PC3’s FastEthernet0/3 — resolved via ARP)

---

## 🔹 B. SW1 → PC3
- **Source MAC:** `aaaa` (PC1)
- **Destination MAC:** `3333` (PC3)

---

## 🧪 Verification Steps
- Sent a ping from PC1 to PC3 to trigger ARP.
- On PC1: ran `ipconfig /all` to identify the source MAC.
- On PC3: also ran `ipconfig /all` to verify its MAC.
- Used **Packet Tracer Simulation Mode** to inspect the Ethernet frame details.

---

## 🧠 Key Takeaway
When two hosts are in the same VLAN/subnet:
- No router is involved.
- The MAC address of the destination host is resolved via ARP.
- The source and destination MAC addresses remain consistent across the LAN.

