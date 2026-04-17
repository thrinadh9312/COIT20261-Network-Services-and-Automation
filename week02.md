# Week 02 – Network Configuration and Connectivity using GNS3

## Student Name: Thrinadh

## Student ID: 12313659

---

# 1. Introduction

In this task, a local area network (LAN) was designed and implemented using GNS3. The objective was to configure multiple Linux-based end devices and establish successful communication between them. Tiny Core Linux was used as the host operating system for all nodes, and an Ethernet switch was used to interconnect the devices.

The experiment demonstrates fundamental networking concepts including IP configuration, subnetting, Layer 2 switching, and ICMP-based connectivity testing. This implementation also demonstrates how Layer 2 devices operate within a broadcast domain and how IP addressing enables logical communication between hosts. The experiment highlights the interaction between physical connectivity and logical network configuration.

---

# 2. Network Topology Design

The network consists of four Linux-based PCs connected to a central Ethernet switch. All devices are placed within the same subnet to enable direct communication without routing.

## Topology Overview:

* 4 × Tiny Core Linux hosts
* 1 × Ethernet switch
* Star topology configuration

**Screenshot: Network Topology**
![Network Topology](screenshots/Network%20Topology.png)

**Explanation:**
This topology represents a simple Layer 2 network where all hosts are connected to a central switch. Since all devices are configured within the same subnet, communication occurs directly through MAC address resolution using ARP without requiring a router.

---

# 3. GNS3 VM Configuration

The GNS3 VM was successfully initialized and running, providing the backend virtualization environment required to run QEMU-based Linux instances.

**Screenshot: GNS3 VM Running**
![GNS3 VM](screenshots/GNS3%20VM%20Running.png)

**Explanation:**
The screenshot confirms that the GNS3 VM is operational, with a valid IP address assigned. This ensures proper communication between the host system and virtual network devices.

---

# 4. Linux Environment Setup

Tiny Core Linux was installed and used as the operating system for all nodes. Each node was accessed using the VNC interface.

**Screenshot: Tiny Core Linux Desktop**
![Linux Desktop](screenshots/Tiny%20Core%20Linux%20Desktop.png)

**Explanation:**
This confirms that the Linux environment is successfully booted and ready for configuration.

---

# 5. IP Address Configuration

Each Linux node was assigned a unique IP address within the same subnet (10.1.1.0/24) using the `ifconfig` command.

## IP Address Table:

| Device | IP Address | Subnet Mask   |
| ------ | ---------- | ------------- |
| PC1    | 10.1.1.1   | 255.255.255.0 |
| PC2    | 10.1.1.2   | 255.255.255.0 |
| PC3    | 10.1.1.3   | 255.255.255.0 |
| PC4    | 10.1.1.4   | 255.255.255.0 |

### Configuration Command:

```bash
sudo ifconfig eth0 10.1.1.X netmask 255.255.255.0 up
```

**Screenshot: IP Configuration**

![PC1 IP](screenshots/pc1\(ip\).png)
![PC2 IP](screenshots/pc2\(ip\).png)
![PC3 IP](screenshots/pc3\(ip\).png)
![PC4 IP](screenshots/pc4\(ip\).png)

**Explanation:**
The screenshots verify that each device has been assigned a correct IP address and that the network interface (eth0) is active. The IP addresses were assigned within the private IPv4 range 10.1.1.0/24, ensuring all devices belong to the same broadcast domain. The subnet mask 255.255.255.0 defines the network boundary and allows efficient communication between hosts.

---

# 6. Connectivity Testing

Connectivity between devices was verified using the ICMP protocol via the `ping` command.

### Example Command:

```bash
ping 10.1.1.2 -c 5
```

**Screenshot: Ping Test Results**

![Ping Test 1](screenshots/Ping%20Test%20Results_1.png)
![Ping Test 2](screenshots/Ping%20Test%20Results_2.png)

**Explanation:**
The ping command uses the Internet Control Message Protocol (ICMP) to test reachability between hosts. Successful replies indicate that both Layer 2 (MAC address resolution via ARP) and Layer 3 (IP communication) are functioning correctly. The absence of packet loss confirms network reliability and correct configuration.

---

# 7. Results and Analysis

* All devices were able to communicate successfully
* No packet loss was observed during testing
* Round-trip time (RTT) values were low, indicating efficient communication
* The switch correctly forwarded frames between all connected devices

The results confirm that the switch successfully forwards frames based on MAC address tables, and that ARP requests and responses are correctly resolving hardware addresses for communication between hosts.

---

# 8. Conclusion

In conclusion, the network was successfully designed and implemented using GNS3 and Tiny Core Linux. All devices were properly configured with valid IP addresses, and connectivity between nodes was verified through successful ping tests. The experiment effectively demonstrates basic networking principles such as IP addressing, subnetting, and LAN communication.

The successful results confirm that both data link layer (Layer 2) and network layer (Layer 3) operations are functioning efficiently. This experiment reinforces fundamental networking concepts that are essential for real-world network design and troubleshooting.

---

# 9. Limitations and Improvements

This implementation was performed in a simulated environment using GNS3. In a real-world network, additional components such as routers, firewalls, and dynamic routing protocols would be required for scalability and security.

Future improvements could include:

* Implementation of VLANs for network segmentation
* Routing between multiple subnets
* Network performance testing under heavy traffic
* Integration of security mechanisms such as firewalls

---


