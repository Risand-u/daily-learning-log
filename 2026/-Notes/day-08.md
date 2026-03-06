# Day 9 — Inter-VLAN Routing Theory
Date: March 04, 2026
Topic: Inter-VLAN Routing
Stage: Stage 2 — Intermediate
Status: 📖 Currently Learning

---

## What I Did Today
- Learned Inter-VLAN Routing theory
- Understood difference between trunk and access ports
- Understood Router on a Stick concept
- Will build project in Packet Tracer next

---

## What is a VLAN?
VLAN stands for Virtual Local Area Network.
Separates one physical network into multiple
virtual networks.

One physical switch can have:
VLAN 10 → IT Department
VLAN 20 → Office Staff
VLAN 30 → Management

Think of it like walls inside a building.
Each department separated from others.

---

## The Problem With VLANs
VLANs are great for separation but by default
they cannot talk to each other!

VLAN 10 PC → cannot reach → VLAN 20 PC ❌

Sometimes departments need to communicate.
Inter-VLAN Routing fixes this!

---

## What is Inter-VLAN Routing?
Process of allowing different VLANs to
communicate with each other through a router.

Without Inter-VLAN Routing:
VLAN 10 ❌ VLAN 20 ❌ VLAN 30

With Inter-VLAN Routing:
VLAN 10 ✅ Router ✅ VLAN 20 ✅ VLAN 30

---

## Two Methods

Method 1 — Traditional
Each VLAN gets its own physical cable
to a separate router interface.
Simple but uses too many router ports!
Not practical for large networks.

Method 2 — Router on a Stick
All VLANs share ONE cable to router.
Router uses subinterfaces for each VLAN.
More efficient! Only needs one router port.
This is what we will use!

---
