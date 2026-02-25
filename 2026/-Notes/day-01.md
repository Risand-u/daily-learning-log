# Day 1 - February 24, 2026

## Topic: Cisco Networking Basics (Packet Tracer)

---

### What I Learned Today

#### 1. Why Router Type Matters
- **Router-PT** is a basic practice router with non-functional ports — not good for real simulations
- **Cisco 2911** is a real-world router used in companies — has proper working ports
- Always use 2911 for realistic network practice

---

#### 2. Cable Types
- **Copper Straight-Through** → connects *different* devices (Router ↔ Switch, Switch ↔ PC)
- **Copper Crossover** → connects *same* devices (PC ↔ PC, Router ↔ Router)
- Rule: different devices = straight-through

---

#### 3. Router vs Switch
- **Router** = the front gate, connects network to outside world, decides where data goes
- **Switch** = the hallway, lets multiple devices connect and talk to each other

---

#### 4. Why Connections Failed at First (3 Reasons)
1. Wrong router (Router-PT had no functional ports)
2. Port was down → had to type `no shutdown` to activate it
3. Cable was loose → had to reconnect properly

---

#### 5. IP Addresses
Every device needs an IP like every house needs an address.

| Device | IP Address |
|--------|-----------|
| Router | 192.168.1.1 |
| PC1 | 192.168.1.10 |
| PC2 | 192.168.1.20 |

All in the same range `192.168.1.x` so they can communicate — like houses on the same street.

---

#### 6. `no shutdown` Command
- Cisco router ports are **OFF by default** for safety
- `no shutdown` = turning the port on
- Without it, port stays dead even with cable connected

---

#### 7. GigabitEthernet vs FastEthernet
| Term | Speed | Used In |
|------|-------|---------|
| FastEthernet (fa) | 100 Mbps | Older/basic routers |
| GigabitEthernet (gig) | 1000 Mbps | Modern routers like 2911 |

---

#### 8. Port Numbering (0/0, 0/1, 1/0...)
Think of it as a **building with floors and rooms:**
- First number = Module (floor)
- Second number = Port (room)

| Port | Means |
|------|-------|
| Gig0/0 | Module 0, Port 0 (first port) |
| Gig0/1 | Module 0, Port 1 (second port) |
| Gig1/0 | Module 1, Port 0 |

**Rule:** Always start from 0/0 and go up.

---

#### 9. What I Built Today
A mini office network:
```
Router (Gig0/0) ──── Switch (Fa0/1)
                      Switch (Fa0/2) ──── PC1
                      Switch (Fa0/3) ──── PC2
```
- Router = security guard at the front gate
- Switch = hallway connecting all rooms
- PCs = people in the rooms
- **All devices communicated successfully ✅**

---

### Key Takeaways
- Use Cisco 2911, not Router-PT
- Always type `no shutdown` to activate router ports
- Same range IP addresses = devices can talk to each other
- Port numbering = module/port like floors and rooms in a building
