# Day 17 - VLANs (Part 2) Lab

## Objective
This lab expands on VLAN concepts by implementing trunk links, native VLAN configuration, and inter-VLAN routing using the router-on-a-stick method. All devices across multiple VLANs should be able to communicate.


![image](https://github.com/user-attachments/assets/6f39c343-2218-4493-82c4-ea3b6eb9ef6d)


## Network Overview

| VLAN   | Name        | Subnet            | Example PC IPs      | Gateway IP         |
|--------|-------------|-------------------|----------------------|---------------------|
| VLAN10 | Engineering | 10.0.0.0/26       | 10.0.0.1 – .4        | 10.0.0.62           |
| VLAN20 | HR          | 10.0.0.64/26      | 10.0.0.65            | 10.0.0.126          |
| VLAN30 | Sales       | 10.0.0.128/26     | 10.0.0.129 – .130    | 10.0.0.190          |

## Tasks Performed

1. **PC Configuration:**
   - Assigned appropriate IP addresses and subnet masks.
   - Used the **last usable IP** of each subnet as the default gateway.

2. **Access Port Configuration:**
   - Assigned SW1 and SW2 access ports to their respective VLANs for connected PCs.

3. **VLAN Setup:**
   - Created VLANs 10, 20, and 30 on both switches.
   - Used VLAN 99 as an unused/native VLAN (optional per design).
   - Named VLANs appropriately: Engineering, HR, Sales.

4. **Trunk Link Configuration (SW1 ↔ SW2):**
   - Allowed only VLANs 10, 20, and 30 on the trunk.
   - Configured native VLAN (e.g., VLAN 99) on trunk port.

5. **Router-on-a-Stick (R1 ↔ SW2):**
   - Configured subinterfaces on R1 for VLANs 10, 20, and 30.
   - Assigned gateway IPs to each subinterface.
   - Enabled trunking on the SW2 port connected to R1.

6. **Testing:**
   - Verified full connectivity across all PCs in different VLANs.
   - Confirmed inter-VLAN routing through R1.
   - Used `ping` and Packet Tracer’s Simulation Mode to trace packets.

## Tools Used
- Cisco Packet Tracer

## Key Concepts Practiced
- VLAN access and trunk port configuration
- Inter-switch trunking and native VLANs
- Inter-VLAN routing using router-on-a-stick
- Subinterface creation on routers
