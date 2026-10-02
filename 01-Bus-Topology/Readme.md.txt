# Lab 01: Bus Topology (Cisco Packet Tracer)

A hands-on networking lab that demonstrates how a bus topology works, built and tested in Cisco Packet Tracer.

---

## Objective

- Build a bus topology in which all devices share a single backbone cable
- Assign IP addresses to every device in the same network
- Verify connectivity between all devices using ping
- Understand the advantages and limitations of a bus topology

---

## Topology

![Bus Topology](topology.png)

---

## What is a Bus Topology?

In a bus topology, all devices (nodes) connect to one shared communication line called the bus or backbone. Data sent by one device travels along the bus and is received by the device it is addressed to. Both ends of the bus are normally closed with terminators to stop signals reflecting back.

---

## Devices Used

| Device | Quantity | Purpose |
|--------|----------|---------|
| PC | [number] | End devices that send and receive data |
| Hub / Switch | [number] | Connection point used to simulate the shared bus in Packet Tracer |
| Cables | [type] | Links between devices |

---

## IP Addressing Plan

| Device | IP Address | Subnet Mask |
|--------|-----------|-------------|
| PC0 | 192.168.1.1 | 255.255.255.0 |
| PC1 | 192.168.1.2 | 255.255.255.0 |
| PC2 | 192.168.1.3 | 255.255.255.0 |
| PC3 | 192.168.1.4 | 255.255.255.0 |

---

## How to Run This Lab

1. Install Cisco Packet Tracer.
2. Open bus_topology.pkt from this folder.
3. Click each PC, go to Desktop > IP Configuration, and check the address.
4. Open Desktop > Command Prompt on any PC and run the tests below.

---

## Testing and Results

| Test | Command | Expected Result |
|------|---------|-----------------|
| PC0 to PC1 | ping 192.168.1.2 | Replies received, 0% loss |
| PC0 to PC3 | ping 192.168.1.4 | Replies received, 0% loss |
| PC2 to PC1 | ping 192.168.1.2 | Replies received, 0% loss |

---

## Advantages of Bus Topology

- Simple and cheap to set up
- Needs less cable than star or mesh
- Easy to add a new device to the backbone
- Good for small, temporary networks

## Disadvantages of Bus Topology

- A fault in the main cable can bring down the entire network
- Performance drops as more devices are added, because they share one channel
- Collisions are likely when several devices transmit at once
- Hard to troubleshoot and not secure, since all data travels on the same line
- Rarely used in modern networks, which mostly use star topology

---

## Files in This Folder

01-bus-topology/
  README.md
  bus_topology.pkt

---

## Tools

- Cisco Packet Tracer [add your version]

---