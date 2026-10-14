# Enterprise Network Security Implementation (Fortinet Capstone Project)

## 📌 Project Overview
This repository contains the complete design, implementation, and verification of a secure multi-site enterprise network built on **PNETLab**. The architecture features FortiGate Next-Generation Firewalls (NGFW) in High Availability (HA), Cisco Core/Access Switches, and Routers.

## 📐 Network Topology
![Topology](Topologies/pnet_lab_topology.png)

## 📊 IP Addressing & VLAN Scheme
- **HQ Site:**
  - User VLAN 10: `10.10.10.0/24` (Gateway: `10.10.10.1`)
  - Server VLAN 20: `10.10.20.0/24` (Gateway: `10.10.20.1`)
  - Management VLAN 30: `10.10.30.0/24` (Gateway: `10.10.30.1`)
- **Branch 1 Site:** User VLAN (`10.20.10.0/24`), Server VLAN (`10.20.20.0/24`)
- **Branch 2 Site:** User VLAN (`10.30.10.0/24`), Server VLAN (`10.30.20.0/24`)
- **SSL-VPN Remote Pool:** `10.200.10.100 - 10.200.10.200`

## ✨ Features Implemented
- [x] **HA Active-Passive Cluster:** Configured on HQ FortiGates with primary/secondary failover.
- [x] **Site-to-Site IPsec VPN:** Tunnels established between HQ <-> Branch 1 & HQ <-> Branch 2.
- [x] **Remote Access SSL-VPN:** Configured for secure user access with full portal permissions.
- [x] **Security Profiles (UTM):** Antivirus, Web Filter, DNS Filter, IPS, and Application Control applied.
- [x] **Automation Stitches (Bonus):** Automated triggers and Discord/Log alerts for HA Failover events.

## 📁 Repository Structure
```text
├── Topologies/           # Topology diagrams
├── Configs/              # Configuration files (.conf) for Firewalls & Switches
├── Screenshots/          # Verification proofs (HA, VPN, SSL, Ping Tests)
└── README.md             # Project documentation-Network-Security
