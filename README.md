# 🏨 Modern Hotel Network

## About the project

This is a Cisco Packet Tracer project based on a Modern Hotel network design. I built the network around three floors, with each department placed into its own VLAN and network.

The main goal was to build a network where the different departments could communicate with each other while keeping the network organised through VLANs. The project also focuses on routing, DHCP, wireless connectivity, SSH remote access and basic switch security.

## 🌐 Network topology

![Modern Hotel Network Topology](./Hotel%20Network.png)

The topology uses three routers located in the IT server room. Each floor has its own switch and the routers are connected to each other using serial links.

The network also includes wireless access points, laptops, phones and printers for the different departments.

## 🏢 Floor layout

### 1st Floor

| Department | VLAN | Network |
|---|---:|---|
| Reception | 80 | `192.168.8.0/24` |
| Store | 70 | `192.168.7.0/24` |
| Logistics | 60 | `192.168.6.0/24` |

### 2nd Floor

| Department | VLAN | Network |
|---|---:|---|
| Finance | 50 | `192.168.5.0/24` |
| HR | 40 | `192.168.4.0/24` |
| Sales and Marketing | 30 | `192.168.3.0/24` |

### 3rd Floor

| Department | VLAN | Network |
|---|---:|---|
| Admin | 20 | `192.168.2.0/24` |
| IT | 10 | `192.168.1.0/24` |

## 🔌 Router connections

The routers are connected using the following networks:

| Link | Network |
|---|---|
| Router connection 1 | `10.10.10.0/30` |
| Router connection 2 | `10.10.10.4/30` |
| Router connection 3 | `10.10.10.8/30` |

OSPF is used as the routing protocol to advertise the different networks between the routers.

## 📡 Wireless network

Each floor has wireless connectivity for laptops and phones. This gives the hotel staff a way to connect mobile devices while still keeping the departments organised within the network design.

## 🖨️ Printers

Each department is expected to have its own printer. This allows the project to represent a more realistic hotel environment where staff need access to shared department resources.

## 🔐 Network security

One of the parts I worked on in this project was securing the IT department switch.

The IT department has a Test PC connected to FastEthernet 0/1. Port security is configured so that the switch can learn the MAC address using the sticky method. The violation mode is set to shutdown.

This means the port is intended to accept the approved Test PC and shut down if an unauthorised device is connected.

## 🔑 SSH remote access

SSH is configured on the routers so that remote management can be performed securely.

The IT department also has a Test PC that can be used to connect to the router remotely through SSH. This was included as part of the project requirements and gives the network a practical remote management feature.

## 📋 Project requirements

The original assignment required the following:

1. Three routers connecting the three floors.

2. Serial DCE connections between the routers.

3. Router networks using `10.10.10.0/30`, `10.10.10.4/30` and `10.10.10.8/30`.

4. One switch on each floor.

5. WiFi networks for laptops and phones on each floor.

6. A printer for each department.

7. A separate VLAN and network for each department.

8. OSPF routing between the routers.

9. Dynamic IP addressing through DHCP.

10. Communication between devices across the network.

11. SSH configuration on all routers.

12. SSH testing from the IT department Test PC.

13. Port security on the IT department switch using sticky MAC learning and shutdown violation mode.

## 🧪 Testing

The network can be tested in Cisco Packet Tracer by checking whether devices receive the correct IP addresses through DHCP and whether devices on different networks can communicate.

Ping tests can be used between departments to confirm that routing is working correctly.

SSH can be tested from the IT Test PC to confirm remote router access.

The IT switch can also be tested by connecting the approved Test PC to FastEthernet 0/1 and checking the learned sticky MAC address.

## 📚 Original project requirements

The assignment pages are included in the repository for reference.

### Requirements page 1

![Hotel Network Requirements Page 1](./Hotel%20Question%20pt1.png)

### Requirements page 2

![Hotel Network Requirements Page 2](./Hotel%20Question%20pt%202.png)

## 🧠 What I learned

Building this project helped me understand how a larger network can be broken down into smaller sections and managed through VLANs.

I also got practical experience with OSPF, DHCP, SSH, wireless networking and switch port security. The port security section was especially useful because it showed me how a simple switch configuration can prevent an unknown device from using a protected port.

## 🚀 Future improvements

If I continue developing this project, I would like to add stronger access control between departments, improve the wireless security and introduce more network monitoring. I would also like to explore how the same hotel design could be expanded without making the network difficult to manage.

## 🛠️ Tools used

Cisco Packet Tracer

Cisco routers

Cisco switches

VLAN

OSPF

DHCP

SSH

Port security

Wireless networking

IPv4 addressing

## 👨‍💻 Project author

**Shadrack Jere**

Aspiring Cybersecurity and Cloud Security Professional

Networking and CCNA Learner
