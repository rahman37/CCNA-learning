# Day 16 - VLANs (Part 1) Lab

## Objective
This lab demonstrates the configuration of multiple VLANs on a switch, assigning appropriate IP addresses, segmenting network traffic, and verifying VLAN isolation using Packet Tracer.

## VLAN Configuration Overview
- **VLAN10 (Engineering):** 10.0.0.0/26  
  - PCs: PC1 (10.0.0.1), PC2 (10.0.0.2)  
  - Gateway: 10.0.0.62  
- **VLAN20 (HR):** 10.0.0.64/26  
  - PCs: PC3 (10.0.0.65), PC4 (10.0.0.66)  
  - Gateway: 10.0.0.126  
- **VLAN30 (Sales):** 10.0.0.128/26  
  - PCs: PC5 (10.0.0.129), PC6 (10.0.0.130)  
  - Gateway: 10.0.0.190  

## Steps Performed

1. **IP Configuration on PCs:**
   - Assigned the first usable IP addresses to PCs.
   - Assigned the last usable address in each subnet as the default gateway (on R1).

2. **Router Interface Configuration:**
   - Used three physical interfaces on R1 (one for each VLAN).
   - Each interface configured with the respective VLAN gateway IP.

3. **Switch VLAN Setup (SW1):**
   - Created and named VLANs: Engineering, HR, Sales.
   - Assigned correct interfaces to each VLAN.
   - Connected each R1 interface to the correct VLAN via SW1.

4. **Connectivity Test:**
   - Verified inter-PC connectivity within each VLAN.
   - Used Packet Tracer's Simulation Mode to observe broadcast traffic.
   - Confirmed that broadcast traffic stayed within its VLAN (no cross-VLAN leakage).

## Tools Used
- Cisco Packet Tracer

## Key Concepts Practiced
- VLAN creation and assignment
- Basic router-on-a-stick concept using separate physical interfaces
- Broadcast domain isolation
- Subnetting and IP planning
- Simulation and connectivity testing
