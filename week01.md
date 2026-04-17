# COIT20261 Network Services and Automation

## Week 01 Portfolio

**Student Name:** Thrinadh
**Student ID:** 12313659
**Project Name:** GNS3-Intro-12313659
**Date:** 14/04/2026

---

## 1. Introduction

This task introduces the use of GNS3 for basic network simulation. The objective is to create a simple network topology, assign a static IP address to a host device, and verify the configuration using command-line tools. This foundational task helps in understanding how devices are configured and identified within a network.

---

## 2. Objective

The main objectives of this task are:

* To create a GNS3 project
* To add a host device (VPCS) to the topology
* To configure a static IP address
* To verify the configuration using commands
* To document the process with screenshots

---

## 3. Tools and Environment

| Tool          | Purpose                        |
| ------------- | ------------------------------ |
| GNS3          | Network simulation software    |
| VPCS          | Lightweight virtual host       |
| Console (CLI) | Configuration and verification |

---

## 4. Network Design

A simple topology was created consisting of:

* **1 × VPCS (PC1)**

Additionally, text annotations were added to display:

* Student Name
* Student ID
* Week Number
* Assigned IP Address

This ensures proper identification and professional presentation.

---

## 5. Implementation Steps

### 5.1 Project Creation

A new project was created with the name:

```
GNS3-Intro-12313659
```

---

### 5.2 Adding Device

A VPCS node (PC1) was added to the workspace to represent a host in the network.

---

### 5.3 Starting the Device

The node was started using the start button in GNS3, making it active and ready for configuration.

---

### 5.4 IP Address Configuration

The following command was used to assign a static IP address:

```
ip 10.10.1.1/24
```

#### Explanation:

* `10.10.1.1` → IP address assigned to the device
* `/24` → Subnet mask (255.255.255.0)
* This ensures the device can be uniquely identified in the network

---

### 5.5 Verification

To verify the configuration, the following command was used:

```
show ip
```

#### Output:

The output confirmed:

* IP Address: 10.10.1.1/24
* Gateway: 0.0.0.0

This indicates that the IP was successfully configured.

---

## 6. Screenshots (Evidence)

### 6.1 Network Topology

**File Name:** `Week01-Network.png`

This screenshot shows:

* PC1 (VPCS)
* Project workspace
* Text annotations:

  * Name: Thrinadh
  * Student ID: 12313659
  * Week 01
  * IP: 10.10.1.1
![Network Topology](screenshots/Week01-Network.png)
---

### 6.2 Console Output

**File Name:** `Week01-Console.png`

This screenshot shows:

* Command execution:

  ```
  ip 10.10.1.1/24
  show ip
  ```
* Output displaying:

  ```
  10.10.1.1/24
  ```

![Console Output](screenshots/Week01-Console.png)

---

## 7. Technical Explanation

IP addressing is a fundamental concept in networking. Each device must have a unique IP address to communicate within a network.

* A **static IP address** is manually assigned and remains constant
* The **subnet mask (/24)** defines the network boundary
* Devices within the same subnet can communicate directly
* The **show ip** command is used to verify configuration

Additionally, correct IP configuration is essential because without it, devices cannot communicate or exchange data within a network.

---

## 8. Learning Outcomes

From this task, I learned:

* How to create a project in GNS3
* How to add and manage network devices
* How to configure a static IP address
* How to verify configuration using commands
* The importance of IP addressing in networking

---

## 9. Reflection

Initially, I faced some difficulty understanding how to correctly configure and verify the IP address. However, after practicing the commands and checking the output, I gained a clear understanding of the process. This task improved my confidence in using GNS3 and basic networking concepts. It also highlighted the importance of verification to ensure correct configuration.

---

## 10. Conclusion

In conclusion, the task was successfully completed by creating a GNS3 project, configuring a static IP address on a host device, and verifying it using command-line tools. This task provided a strong foundation for understanding basic networking concepts and prepares for more advanced topics in future weeks.

---
