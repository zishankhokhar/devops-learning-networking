## Networking Fundamentals

### 🌐 What Networking Is
Networking is the system that allows computers and devices to communicate with each other.
It involves:
- Addresses (IP, MAC)
- Devices (routers, switches, firewalls)
- Protocols (TCP, UDP, HTTP)
- Ports (80, 443, 22, etc.)
At its core, networking is structured communication between machines.

### 🧑‍💻 Why Networking Matters in DevOps
Networking is everywhere in DevOps:
- EC2 instances need IPs and security groups
- Kubernetes uses networking internally (pods, services, ingress)
- Docker containers expose ports
- DNS routes traffic to services
- Load balancers, VPCs, subnets — all networking
- Most cloud issues are networking issues
Understanding networking makes you a better engineer and troubleshooter.

### 🔑 Key Concepts
IP Address
A unique identifier for a device on a network.
Example: 192.168.1.10

MAC Address
A hardware-level identifier burned into the network card.
Example: 00:1A:2B:3C:4D:5E

Ports
Logical communication endpoints.
Examples:
- 80 → HTTP
- 443 → HTTPS
- 22 → SSH

Protocols
Rules for communication.
- TCP → reliable, connection-based
- UDP → fast, connectionless

LAN vs WAN
- LAN → Local network (home, office)
- WAN → Wide network (internet)

### 🛠️ Useful Commands
Test connectivity
ping google.com

Check HTTP response headers
curl -I http://example.com

Check your public IP
curl ifconfig.me

### 💡 What Finally Clicked
Networking is not complicated — it’s a set of building blocks:
- Devices need addresses
- Communication uses ports
- Data follows protocols
- DNS translates names → IPs
- Routers move traffic between networks
Once you understand these basics, everything else becomes easier.