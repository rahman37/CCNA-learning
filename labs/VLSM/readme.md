# Day 15 - VLSM (Variable Length Subnet Masking) Lab

## Objective
This lab demonstrates the use of Variable Length Subnet Masking (VLSM) to efficiently subnet a given IP block and configure static routing for full connectivity in a multi-LAN topology.

## Topology Overview
- **Base Network:** 192.168.5.0/24
- **Subnet Requirements:**
  - LAN1: 45 hosts
  - LAN2: 64 hosts
  - LAN3: 14 hosts
  - LAN4: 9 hosts
  - Point-to-point link between R1 and R2 (2 hosts)

## IP Addressing Plan (VLSM)

| Subnet | Purpose               | Needed Hosts | Subnet Used       | Subnet Mask | Router IP (last usable) | PC IP (first usable) |
|--------|------------------------|--------------|-------------------|-------------|--------------------------|----------------------|
| 1      | LAN2                  | 64           | 192.168.5.0/26    | 255.255.255.192 | 192.168.5.62             | 192.168.5.1          |
| 2      | LAN1                  | 45           | 192.168.5.64/26   | 255.255.255.192 | 192.168.5.126            | 192.168.5.65         |
| 3      | LAN3                  | 14           | 192.168.5.128/28  | 255.255.255.240 | 192.168.5.142            | 192.168.5.129        |
| 4      | LAN4                  | 9            | 192.168.5.144/28  | 255.255.255.240 | 192.168.5.158            | 192.168.5.145        |
| 5      | R1 <-> R2 link        | 2            | 192.168.5.160/30  | 255.255.255.252 | R1: 192.168.5.161, R2: 192.168.5.162 | — |

## Configuration Summary

### Router Interfaces
- Assigned last usable IP address of each subnet to the corresponding router interface.
- Point-to-point link configured between R1 and R2.

### PC Interfaces
- Assigned the first usable IP address in each LAN subnet to the connected PC.

### Routing
- Static routes configured on both R1 and R2 to enable inter-LAN communication across routers.

## Verification
- Verified connectivity using `ping` between all PCs in different LANs.
- Confirmed correct routing table entries and IP reachability.

## Tools Used
- Cisco Packet Tracer

## Learning Outcomes
- Efficient IP address allocation using VLSM
- Subnet planning and documentation
- Static routing configuration
- Network connectivity verification
