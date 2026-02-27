# Day 4 — Review and Revision
Date: February 27, 2026
Topic: Reviewing Past Topics
Stage: Stage 1 — Beginner
Status: ✅ Completed

---

## What I Did Today
- Reviewed and restudied all previous topics
- Cleared confusion about Network Address,
  Broadcast Address and Default Gateway
- Strengthened understanding of subnetting concepts
- Reviewed DHCP configuration and how it works

---

## Things I Restudied

### IP Addressing
Every device needs an IP address like a home address.
It tells other devices where to send data.

### Subnet Mask
Tells the device which part of IP is the network
and which part is the device.
255.255.255 = Network part
0           = Device part

### Important Subnet Terms

Network Address
192.168.1.0
- First address of the subnet
- Name of the street
- Cannot be given to any device ❌

Broadcast Address
192.168.1.63
- Last address of the subnet
- Like a notice board
- Sends message to ALL devices on network
- Cannot be given to any device ❌

Default Gateway
192.168.1.1
- Always the router
- Like security guard at entrance
- Every device uses this to send data
  outside the network
- First usable IP address ✅

Usable IP Range
192.168.1.1 to 192.168.1.62
- Addresses you can give to real devices
- PCs, laptops, phones etc

### Simple Visual
192.168.1.0  = Street name (nobody lives here) ❌
192.168.1.1  = Router/Gateway (security guard) ✅
192.168.1.2  = PC1 ✅
192.168.1.3  = PC2 ✅
...
192.168.1.62 = Last available PC ✅
192.168.1.63 = Notice board ❌

### Subnetting
Dividing one big network into smaller networks.
Like dividing a building into separate floors.

Before: 192.168.1.0/24 = 254 devices all mixed
After:
192.168.1.0/26   = IT Department  (62 devices)
192.168.1.64/26  = Office Staff   (62 devices)
192.168.1.128/26 = Management     (62 devices)

### DHCP
Automatically gives IP addresses to devices.
DORA Process:
D = Discover  → PC asks for IP
O = Offer     → Server offers IP
R = Request   → PC accepts IP
A = Acknowledge → Server confirms IP

DHCP gives 4 things automatically:
1. IP Address      → 192.168.1.11
2. Subnet Mask     → 255.255.255.192
3. Default Gateway → 192.168.1.1
4. DNS Server      → 8.8.8.8

DHCP Exclusion:
Reserved IPs DHCP should never give out
ip dhcp excluded-address 192.168.1.1 192.168.1.10

---

## Projects I Have Built So Far
1. Basic Network    → Router, Switch, VLANs, ACL ✅
2. Subnetting       → 3 department subnets ✅
3. DHCP             → Automatic IP assignment ✅

---

## Things That Were Confusing Before
- Network address vs broadcast address
  → Now clear! Network = street name, 
    Broadcast = notice board
- Why first and last IP cannot be used
  → Now clear! Reserved for network 
    identification and broadcast
- Default gateway confusion
  → Now clear! Always the router,
    first usable IP on the network

---

## Simple Summary of Everything So Far
Router    = security guard, connects networks
Switch    = hallway, connects devices
IP        = home address of device
Subnet    = smaller network inside big network
DHCP      = automatic IP giver
Gateway   = door to outside network
Broadcast = notice board for everyone


