# Day 12 - Life of a Packet (CCNA Lab)

This lab demonstrates how MAC addresses change at each hop in a routed network using Packet Tracer.

## 🧪 Objectives
- Trace the MAC address at each segment as ICMP packets travel across multiple routers and LANs.
- Understand ARP behavior, MAC learning on switches, and frame encapsulation/decapsulation.
- Verify results using CLI (`ipconfig /all`, `show interfaces`) and Packet Tracer simulation mode.

## 🖥️ Topology
![image](https://github.com/user-attachments/assets/e4b32f7c-563d-4d31-84bb-6ec0bdcda7b5)


## 🔍 Scenarios

### 1. PC1 pings PC4
- Routed through R1 → R2 → R3 → SW2
- MAC addresses change at every router hop
- See [MAC_trace_PC1_to_PC4.md](./MAC_trace_PC1_to_PC4.md)

### 2. PC1 pings PC3 (Same LAN)
- Only switch involved
- No router hop required
- See [MAC_trace_PC1_to_PC3.md](./MAC_trace_PC1_to_PC3.md)

### 3. PC4 pings PC1 (Reverse Route)
- Routed through R3 → R2 → R1 → SW1
- Validated using simulation mode
- See [MAC_trace_PC4_to_PC1.md](./MAC_trace_PC4_to_PC1.md)

## 📎 How I Verified
- Sent initial pings to populate ARP and MAC tables.
- Used `ipconfig /all` on PCs to get MAC addresses.
- Used `show interfaces G0/x` on routers to find MACs.
- Used Packet Tracer Simulation Mode to confirm MAC changes at each hop.

## 💡 Takeaways
- Every router changes the frame (new MAC headers).
- MACs are only relevant within the current Layer 2 segment.
- ARP resolution is required before traffic can flow.
