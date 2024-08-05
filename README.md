# Pulchowk Campus Network Design

This repository contains the computer network design for Pulchowk Campus, created using Cisco Packet Tracer. The design divides the campus network into four areas, including various departments, hostel blocks, quarters, and servers, ensuring robust communication, security, and efficient routing across different sections.

## Network Overview

### Network Components

- **9 Routers**
- **23 Networks**
- **2 Internal DNS Servers**
- **2 Web Servers**
- **1 DNS and Web Server within the ISP Network**

### Key Features

- **Dynamic Routing:** Implemented using OSPF (Open Shortest Path First) for intercommunication between networks and devices.
- **VLAN Configurations:** Utilized in Teachers Quarters, Girls Hostel, and Boys Hostel for network management.
- **Security Configurations:** Includes passwords and hostnames for all routers, with Telnet enabled.
- **Multipath Connections:** Ensures enhanced network reliability.

## Network Topology

### Area 0 - Backbone
- **CIT Router:** Acts as the backbone router, connecting all area border routers.
  - Internal networks for Library and New Canteen.

### Area 1
- **Includes ICTC, DOECE, and DOE networks.**
  - Web server handling requests at `exam.edu.np`.

### Area 2
- **Encompasses Civil, Mechanical, Aero, and Applied Science departments.**
  - Local DNS server for internal name resolution.

### Area 3
- **Comprises Boys Hostel, Girls Hostel, and Teachers Quarters.**
  - Web server handling requests at `pcampus.edu.np`.
  - DNS server for local name resolution.

### ISP Network
- **Connects to Pulchowk network via the CIT area border router.**
  - Root DNS server and web server resolving requests at `gmail.com`.

## Server Details

### Internal Servers
- **DNS Servers:** Located in Area 2 and Area 3.
- **Web Servers:** Located in Area 1 (`exam.edu.np`) and Area 3 (`pcampus.edu.np`).

### ISP Servers
- **DNS Server:** Root DNS server in the ISP network.
- **Web Server:** Resolves requests at `gmail.com`.

## Network Security

- **Console Password:** `cisco`
- **Privileged Access Mode Password:** `class`
- **Telnet Password:** `network`
- **Router Naming Convention:** Indexed using names (e.g., `rajesh_1`).
- **Telnet Access:** Configured for all routers.

## IP Addressing and Subnetting

- **Chosen IP Pool:** `128.128.0.0/20`

### Area IP Details
- **Area 1:** `128.128.8.0/22` (Includes ICTC, DOECE, WEB SERVER)
- **Area 2:** `128.128.4.0/22` (Includes Civil, Mechanical, DNS SERVER, Applied Science, Aero)
- **Area 3:** `128.128.0.0/22` (Includes WEB SERVER, Boys Hostel, DNS SERVER, Quarters, Girls Hostel)
- **Area 0:** `128.128.12.0/23` (Includes Library, Canteen)
- **Inter-Area Router Networks:** `128.128.14.0/23`
- **ISP Router Networks:** `128.129.0.0/30` (DNS Server) and `128.129.0.4/30` (Web Server)
- **Complete IP details in PDF**

## Remarks

This network design for Pulchowk Campus may not be fully reflective of the actual Pulchowk network, but it demonstrates how large-scale networks can be effectively designed and implemented in the real world.

## Packet Tracer File

The complete network design with all configurations is available in the Packet Tracer file included in this repository.

## Network Images and Demo Video

### Demo Video
![video](https://github.com/user-attachments/assets/4556b053-488d-4665-a3ee-4471aad7e8f4)

### Images
![image](https://github.com/user-attachments/assets/759219be-e793-4f45-89ee-75576aa887c6)
![image](https://github.com/user-attachments/assets/7509e079-2a40-45ea-9c36-efee605984e6)
![image](https://github.com/user-attachments/assets/6f69cdc9-cf72-412a-a165-bed47951881e)

---

Feel free to clone this repository and use the provided Packet Tracer file to explore the network design in more detail.
