## Routing

### 🌍 What Routing Is
Routing is the process of moving data from one network to another.
A router decides where packets should go based on IP addresses.
If switching is “local delivery”, routing is “sending mail to another city”.

### Why Routing Matters in DevOps
Routing is everywhere in cloud engineering:
- EC2 instances live inside subnets and VPCs
- Internet traffic flows through Internet Gateways
- Kubernetes uses routing internally between pods and nodes
- Load balancers route traffic to backend servers
- VPNs and corporate networks rely on routing tables
If routing breaks, nothing reaches its destination.

### 🧩 Key Routing Concepts
Routing Table
A list of rules that tells a router where to send packets.
Check your routing table:
netstat -rn
or
ip route

Default Gateway
The router your machine uses to reach the internet.
Example:
default via 192.168.1.1

Hop
Each router a packet passes through.

### 🛣️ Types of Routing
1. Static Routing
Manually configured routes.
Used in small networks or simple setups.

Pros: predictable
Cons: not scalable

2. Dynamic Routing
Routers automatically share route information.
Uses routing protocols like:
- OSPF (Open Shortest Path First)
- BGP (Border Gateway Protocol)
- RIP (Routing Information Protocol)
Used in large networks and the internet.

### 🔄 Common Routing Protocols
OSPF
- Internal routing
- Fast convergence
- Used inside organisations

BGP
- The protocol that runs the entire internet
- Connects ISPs and large networks
- Used by AWS, Azure, Google Cloud

RIP
- Older protocol
- Rarely used today

### 🛠️ Routing Troubleshooting Tools
Traceroute
Shows the path packets take.
macOS/Linux:
traceroute google.com

Windows:
tracert google.com

Ping
Checks if a destination is reachable.
ping 8.8.8.8

Curl
Checks if an application is responding.
curl -I http://example.com

### 💡 What Finally Clicked
Routing is just decision-making:
- “If the destination is local → send directly”
- “If it’s outside the network → send to the gateway”
- “If the gateway doesn’t know → forward to another router”
In cloud environments, routing tables are software-defined, not physical devices.