# MAC Address Flow: PC4 to PC1

## 🧭 Scenario
This trace follows an ICMP Echo Request from **PC4 (192.168.3.1)** to **PC1 (192.168.1.1)**. Since this crosses multiple routers, the MAC address is rewritten at every Layer 2 segment.

---

## 🔹 A. PC4 → SW2
- **Source MAC:** PC4 FastEthernet0/1 (e.g., `4444`)
- **Destination MAC:** R3 G0/1 (`ffff`) — PC4’s default gateway

---

## 🔹 B. SW2 → R3
- Same as above:
  - Src: `4444`
  - Dst: `ffff`

---

## 🔹 C. R3 → R2
- **Source MAC:** R3 G0/0 (`eeee`)
- **Destination MAC:** R2 G0/1 (`dddd`)

---

## 🔹 D. R2 → R1
- **Source MAC:** R2 G0/0 (`cccc`)
- **Destination MAC:** R1 G0/1 (`bbbb`)

---

## 🔹 E. R1 → SW1
- **Source MAC:** R1 G0/0 (`aaaa`)
- **Destination MAC:** PC1 (`1111`)

---

## 🔹 F. SW1 → PC1
- Same as above:
  - Src: `aaaa`
  - Dst: `1111`

---

## 🧪 Verification Steps
- Sent an initial ping from PC4 to PC1 to complete ARP resolution.
- Verified MACs using:
  - `ipconfig /all` on PCs
  - `show interfaces` on routers
- Used **Packet Tracer Simulation Mode** to inspect the MAC addresses on each Ethernet frame.

---

## 🧠 Key Takeaway
Even though the IP source and destination remain constant end-to-end, the **MAC addresses are rewritten at every Layer 2 segment** by routers to reflect the **next-hop** in the path.

