
# 🛡️ Cybersecurity Virtual Lab Setup

<p align="center">
  <img src="https://img.shields.io/badge/Domain-Cybersecurity-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/Platform-VirtualBox-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Operating%20System-Kali%20Linux-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Project-01-success?style=for-the-badge">
</p>

## 1. Introduction

This project demonstrates the development of a virtual cybersecurity laboratory using Oracle VirtualBox and Kali Linux.

The laboratory provides a dedicated environment for learning computer security, understanding network communication, and performing authorized security experiments.

The main idea is to create a virtual environment where different operating systems can operate and communicate through a private network.

## 2. Project Goals

The project aims to achieve the following:

- Establish a virtual machine environment.
- Install and configure Kali Linux.
- Set up a private virtual network.
- Understand IP addressing and network communication.
- Configure internet connectivity.
- Test network functionality.
- Create a system recovery snapshot.
- Develop practical cybersecurity skills.

## 3. Software and Technologies

The following tools are required for this project:

| Tool | Purpose |
|---|---|
| Oracle VirtualBox | Virtual machine management |
| Kali Linux | Cybersecurity operating system |
| 7-Zip | Extracting installation files |
| Nmap | Network discovery and scanning |
| Windows | Host operating system |

## 4. Virtual Lab Design

The laboratory consists of a host computer and a Kali Linux virtual machine.

### Network Structure

```text
       HOST COMPUTER
        (Windows OS)
             |
       VirtualBox
             |
        NAT Network
        10.0.0.0/24
             |
       Kali Linux VM
         10.0.0.2
             |
       Gateway: 10.0.0.1
```

Additional virtual machines can be connected to the same network for future authorized testing.

## 5. System Requirements

| Component | Configuration |
|---|---|
| Host Operating System | Windows 10 |
| Virtualization Software | VirtualBox |
| Guest Operating System | Kali Linux |
| Allocated RAM | 2 GB |
| Network Mode | NAT Network |
| Network Address | 10.0.0.0/24 |
| Kali IP Address | 10.0.0.2 |
| Gateway | 10.0.0.1 |
| DNS Server | 8.8.8.8 |

*Note: These are example configurations. Replace them with your actual system specifications.*

## 6. Implementation Process

### Step 1: Prepare the Installation Environment

Download and install the necessary software, including VirtualBox and 7-Zip.

Download Kali Linux from its official website.

### Step 2: Configure VirtualBox

Install Oracle VirtualBox and prepare it to host the Kali Linux virtual machine.

### Step 3: Set Up the Virtual Network

Create a NAT Network in VirtualBox.

Network settings:

- Network Name: CyberLab
- IPv4 Network: 10.0.0.0/24
- DHCP: Enabled
- IPv6: Disabled

### Step 4: Import Kali Linux

Import the downloaded Kali Linux virtual machine into VirtualBox.

Allocate the required memory and connect its network adapter to the created NAT Network.

### Step 5: Configure Network Settings

Configure the Kali Linux network interface.

Example:

```text
IP Address: 10.0.0.2
Subnet Mask: 255.255.255.0
Gateway: 10.0.0.1
DNS: 8.8.8.8
```

### Step 6: Save the Virtual Machine State

Create a snapshot after completing the initial setup.

Snapshot Name:

`CyberLab Initial Configuration`

This snapshot provides a recovery point if future experiments affect the virtual machine.

## 7. Network Testing

After configuration, perform the following checks:

| Test | Command | Purpose |
|---|---|---|
| IP Verification | `ip addr` | Display IP configuration |
| Gateway Test | `ping 10.0.0.1` | Check gateway connectivity |
| Internet Test | `ping 8.8.8.8` | Test external connectivity |
| DNS Test | `nslookup google.com` | Verify DNS resolution |
| Nmap Test | `nmap --version` | Verify Nmap installation |

### Expected Results

The network tests should confirm that:

- Kali Linux has the expected IP address.
- The gateway is reachable.
- Internet connectivity is available.
- DNS resolution works correctly.
- Nmap is installed and accessible.

## 8. Challenges and Troubleshooting

During the setup process, some technical challenges may occur.

### Challenge 1: Virtual Machine Fails to Start

**Possible Cause:** Hardware virtualization is disabled.

**Solution:** Check BIOS/UEFI settings and enable Intel VT-x or AMD-V where supported.

### Challenge 2: Network Connectivity Problems

**Possible Cause:** Incorrect network adapter or IP configuration.

**Solution:**
- Check the VirtualBox network adapter.
- Verify the IP address.
- Check the default gateway.
- Restart the network connection.

### Challenge 3: Internet Access Failure

**Possible Cause:** Incorrect DNS or NAT Network configuration.

**Solution:** Verify DNS settings and confirm that the virtual network is configured correctly.

## 9. Skills and Knowledge Acquired

This project provides practical experience in:

1. Virtual machine installation and management.
2. Linux operating system configuration.
3. IPv4 networking.
4. NAT Network architecture.
5. Network connectivity testing.
6. Basic cybersecurity laboratory preparation.
7. Technical troubleshooting.
8. Project documentation.

## 10. Security Considerations

This virtual laboratory is intended for educational purposes.

All security testing must be conducted on systems owned by the user or where explicit authorization has been granted.

The virtual environment should be configured carefully to prevent unintended testing against external systems.

## 11. Conclusion

The project demonstrates how virtualization technology can be used to establish a basic cybersecurity learning environment.

Through the installation of VirtualBox and Kali Linux, configuration of a private network, and performance of network verification tests, a foundation for future cybersecurity practical exercises has been established.

## 12. References

- VirtualBox: https://www.virtualbox.org/
- Kali Linux: https://www.kali.org/get-kali/
- 7-Zip: https://www.7-zip.org/
- Nmap: https://nmap.org/

---

## 13. Project Author

**Name:** [ABUBAKAR KHAMIS ALI]

**Course:** Cybersecurity

**Project:** Virtual Cybersecurity Laboratory Setup

**Institution:** [NETWORKWALKS]

**GitHub:** [lalinho17]

