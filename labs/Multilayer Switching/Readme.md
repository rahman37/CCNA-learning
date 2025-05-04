# Day 18 - Inter-VLAN Routing with Multilayer Switch (SVI)

## Objective
This lab focuses on replacing Router-on-a-Stick (ROAS) with a multilayer switch performing inter-VLAN routing using Switch Virtual Interfaces (SVIs). The network is also tested for internet connectivity.

## Network Overview

| VLAN   | Name        | Subnet            | PC IPs               | Gateway IP (SVI)    |
|--------|-------------|-------------------|----------------------|----------------------|
| VLAN10 | Engineering | 10.0.0.0/26       | 10.0.0.1 – .4        | 10.0.0.62            |
| VLAN20 | HR          | 10.0.0.64/26      | 10.0.0.65            | 10.0.0.126           |
| VLAN30 | Sales       | 10.0.0.128/26     | 10.0.0.129 – .130    | 10.0.0.190           |
| Point-to-Point | —  | 10.0.0.192/30     | SW2: 10.0.0.193, R1: 10.0.0.194 | —

## Steps Performed

1. **Removed ROAS Configuration:**
   - Removed subinterfaces on R1.
   - Configured a Layer 3 P2P link between SW2 and R1 (10.0.0.192/30).
   - Set SW2's default route to `10.0.0.194` (R1’s IP).

2. **Configured SVIs on SW2:**
   - Created SVIs for VLANs 10, 20, and 30.
   - Assigned last usable IPs as gateways to each SVI:
     - VLAN10 → 10.0.0.62
     - VLAN20 → 10.0.0.126
     - VLAN30 → 10.0.0.190

3. **Verified Inter-VLAN Routing:**
   - Pinged between PCs in different VLANs to confirm SVI-based routing.

4. **Tested Internet Connectivity:**
   - Pinged 1.1.1.1 from PCs and confirmed reachability via R1.
   - Confirmed default routing path from SW2 through R1 to the Internet.

## Tools Used
- Cisco Packet Tracer

## Key Concepts Practiced
- Inter-VLAN routing using multilayer switch SVIs
- Static routing from switch to router
- Point-to-point Layer 3 connection
- Testing internal and external network connectivity
