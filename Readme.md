# 🧠 Network Infrastructure Project: Inter-VLAN Routing, HSRP, and Routing Implementation

## 📌 Overview

This project demonstrates a simulated enterprise network setup incorporating **Inter-VLAN Routing**, **HSRP (Hot Standby Router Protocol)** for gateway redundancy, and **dynamic/static routing** techniques. It was developed as part of a networking course/project to showcase practical knowledge of real-world networking concepts.

---

## 🛠️ Key Features

- ✅ Inter-VLAN Routing via Layer 3 Switch or Router-on-a-Stick
- ✅ HSRP for Redundant Gateway Configuration
- ✅ VLAN Configuration and Management
- ✅ Static or Dynamic Routing (e.g., OSPF/EIGRP)
- ✅ End-to-End Network Communication Between VLANs
- ✅ Simulated Failover Scenarios to Test HSRP

---

## 🧰 Tools & Technologies

- **Cisco Packet Tracer** (or GNS3, if applicable)
- Cisco IOS CLI
- Layer 2/Layer 3 Switches
- Routers
- PCs/Endpoints

---

## 🧩 Topology

![Network Topology](topology.png) <!-- Replace with actual image if available -->

The network topology consists of:
- Multiple VLANs for segmentation (e.g., VLAN 10 - HR, VLAN 20 - Finance, etc.)
- Two routers configured with HSRP for default gateway redundancy
- Switches configured with trunk/access ports
- PCs assigned static IPs within VLANs

---

## 🔧 Configuration Overview

Example of key configurations:

### VLANs
```bash
Switch(config)# vlan 10
Switch(config-vlan)# name HR
Switch(config)# interface range fa0/1 - 10
Switch(config-if-range)# switchport access vlan 10

Inter-VLAN Routing

Router(config)# interface g0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# ip address 192.168.10.1 255.255.255.0


HSRP Configuration

Router1(config-if)# standby 1 ip 192.168.10.254
Router1(config-if)# standby 1 priority 110
Router1(config-if)# standby 1 preempt

Router2(config-if)# standby 1 ip 192.168.10.254
Router2(config-if)# standby 1 priority 90
Router2(config-if)# standby 1 preempt

Routing

Router(config)# ip route 192.168.20.0 255.255.255.0 10.0.0.2

Testing
Verified inter-VLAN communication using ping

Simulated failover by shutting down primary router interface (HSRP tested)

Verified correct routing using traceroute and show ip route

Learning Outcomes
Gained hands-on experience with enterprise-level networking concepts

Understood how HSRP provides redundancy for high availability

Learned VLAN segmentation and router-on-a-stick implementation

Practiced configuring and troubleshooting routing protocols


