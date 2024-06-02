---
{
    "title": "how to ues",
    "description": "",
    "navbar": true,
    "sideBar": true,
    "footer": false,
    "outline": [
        1,
        3
    ],
    "editLink": false,
    "lastUpdated": true,
    "aside": "right",
    "layout": "doc",
    "custom": {},
    "hero": {
        "image": {
            "src": "",
            "alt": "",
            "width": "",
            "height": ""
        },
        "name": "VitePressSimple",
        "text": "quick to config vitePress",
        "description": "",
        "tagline": "",
        "actions": [],
        "features": [],
        "head": []
    }
}
---

### Day 4: Network Configuration and Management

#### Objectives

- Understand basic networking concepts and configurations.
- Learn to configure network interfaces.
- Get familiar with basic network troubleshooting tools.

---

#### 1. Basic Networking Concepts

**IP Addressing**

1. **IP Address**

   - Unique identifier assigned to each device on a network.
   - IPv4: Consists of four octets (e.g., 192.168.1.1).
   - IPv6: Consists of eight groups of hexadecimal digits (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).
2. **Subnet Mask**

   - Determines the network and host portions of an IP address.
   - Common subnet mask for home networks: 255.255.255.0.
3. **Gateway**

   - Device that routes traffic from a local network to other networks or the internet.
4. **DNS (Domain Name System)**

   - Translates domain names (e.g., www.example.com) into IP addresses.

**Network Interfaces**

1. **Ethernet Interface**

   - Wired network connection, typically named `eth0`, `eth1`, etc.
2. **Wireless Interface**

   - Wireless network connection, typically named `wlan0`, `wlan1`, etc.

**Configuring Network Interfaces**

1. **Checking Network Interfaces**

   - View all network interfaces:
     ```bash
     $ ip link show
     ```
2. **Assigning an IP Address**

   - Assign an IP address to an interface:
     ```bash
     $ sudo ip addr add 192.168.1.100/24 dev eth0
     ```
3. **Bringing an Interface Up or Down**

   - Bring up an interface:
     ```bash
     $ sudo ip link set eth0 up
     ```
   - Bring down an interface:
     ```bash
     $ sudo ip link set eth0 down
     ```
4. **Viewing IP Address Configuration**

   - Display IP addresses assigned to all interfaces:
     ```bash
     $ ip addr show
     ```

**Network Configuration Files**

1. **/etc/network/interfaces** (Debian-based systems)

   - Example configuration for a static IP:
     ```plaintext
     auto eth0
     iface eth0 inet static
       address 192.168.1.100
       netmask 255.255.255.0
       gateway 192.168.1.1
     ```
2. **/etc/netplan/** (Ubuntu 18.04+)

   - Example configuration for a static IP:

     ```yaml
     network:
       version: 2
       ethernets:
         eth0:
           dhcp4: no
           addresses:
             - 192.168.1.100/24
           gateway4: 192.168.1.1
           nameservers:
             addresses: [8.8.8.8, 8.8.4.4]
     ```
   - Apply the configuration:

     ```bash
     $ sudo netplan apply
     ```

---

#### 2. Network Troubleshooting Tools

**ping Command**

- Test connectivity to another network device:
  ```bash
  $ ping www.google.com
  ```
- Stop the ping command with `Ctrl + C`.

**ifconfig Command**

- Display or configure network interfaces (deprecated in favor of `ip` command):
  ```bash
  $ ifconfig
  ```

**traceroute Command**

- Display the route packets take to a network host:
  ```bash
  $ traceroute www.google.com
  ```

**netstat Command**

- Display network connections, routing tables, interface statistics:

  ```bash
  $ netstat -tuln
  ```

  - `-tuln`: Show listening TCP and UDP ports.

**nslookup Command**

- Query DNS to obtain domain name or IP address mapping:
  ```bash
  $ nslookup www.google.com
  ```

**curl Command**

- Transfer data to or from a server, useful for testing web services:
  ```bash
  $ curl http://www.example.com
  ```

**Practice Exercises**

**Exercise 1: Basic Network Configuration**

1. Check your current IP address configuration:

   ```bash
   $ ip addr show
   ```
2. Assign a static IP address to `eth0`:

   ```bash
   $ sudo ip addr add 192.168.1.200/24 dev eth0
   ```
3. Bring the `eth0` interface up:

   ```bash
   $ sudo ip link set eth0 up
   ```
4. Verify the new IP address:

   ```bash
   $ ip addr show eth0
   ```

**Exercise 2: Network Troubleshooting**

1. Test connectivity to Google's DNS server:

   ```bash
   $ ping 8.8.8.8
   ```
2. Use `traceroute` to trace the route to www.google.com:

   ```bash
   $ traceroute www.google.com
   ```
3. Display network connections using `netstat`:

   ```bash
   $ netstat -tuln
   ```
4. Perform a DNS lookup for www.google.com:

   ```bash
   $ nslookup www.google.com
   ```

By the end of Day 4, users will have a solid understanding of basic network configuration and management, as well as troubleshooting network issues. These skills are essential for ensuring network connectivity and diagnosing problems in a Linux environment.
