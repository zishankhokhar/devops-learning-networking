## Subnetting & CIDR

### 🧩 What Subnetting Is
Subnetting is the process of splitting a large network into smaller networks.

Example:
A big network like 192.168.1.0/24 can be divided into smaller subnets such as:
- 192.168.1.0/26
- 192.168.1.64/26
- 192.168.1.128/26
- 192.168.1.192/26
Each subnet becomes its own mini‑network.

### 🔢 What CIDR Means
CIDR = Classless Inter‑Domain Routing  
It’s the /number you see in IP ranges.

Example:
192.168.1.0/24

The /24 tells you:
- How many bits are used for the network
- How many IPs are available

### 📏 CIDR Cheat Sheet

CIDR    Total IPs   Usable IPs   Subnet Mask
/24     256         254          255.255.255.0
/25     128         126          255.255.255.128
/26     64          62           255.255.255.192
/27     32          30           255.255.255.224
/28     16          14           255.255.255.240
/29     8           6            255.255.255.248


### 🧮 How to Calculate Subnets
Example:
You have a /24 network and want 4 subnets.

A /24 has 256 IPs.
To split into 4 equal subnets:
- /24 → /26
- Because /26 gives 64 IPs each
- And 64 × 4 = 256

So the subnets become:

1. 192.168.1.0/26
2. 192.168.1.64/26
3. 192.168.1.128/26
4. 192.168.1.192/26

### 🏗️ Subnetting in AWS
AWS VPCs use CIDR blocks like:
10.0.0.0/16

You then create subnets:
- Public subnet: 10.0.1.0/24
- Private subnet: 10.0.2.0/24
- Database subnet: 10.0.3.0/24

Subnetting helps you separate:
- Public vs private resources
- App tiers
- Security boundaries

### 🔄 NAT (Network Address Translation)
NAT allows private IPs to access the internet using one public IP.
Example:
Private subnet → NAT Gateway → Internet
This is why private EC2 instances can run updates without being exposed publicly.

### 🛠️ Useful Commands
Check your IP and subnet:
ip addr

Check routing table:
ip route

### 💡 What Finally Clicked
Subnetting is just math + organisation:
- CIDR tells you how big the network is
- Subnetting divides it into smaller chunks
- AWS uses this everywhere (VPCs, subnets, routing tables)
Once you understand /24, /26, /28, everything else becomes easier.

