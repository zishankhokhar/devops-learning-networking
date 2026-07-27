## 📘 DevOps Networking Reference

A structured, practical reference covering the networking concepts that come up daily in DevOps and cloud engineering — IP addressing, the OSI model, DNS, routing, subnetting, and troubleshooting — with commands and real AWS/Linux examples throughout.

This is written as a reference guide, not a study log: each file explains the concept, why it matters in a DevOps context, and the commands you'd actually run to work with or debug it.

**🔗 See it applied:** the concepts here (DNS, subnetting, routing) are put into practice in [`aws-ec2-nginx-dns`](https://github.com/zishankhokhar/aws-ec2-nginx-dns) — an EC2 deployment with NGINX and a custom domain wired up via Cloudflare DNS.

### 📚 Contents

| # | Topic | Covers |
|---|-------|--------|
| 01 | [Fundamentals](networking/notes/01-fundamentals.md) | IP/MAC addresses, ports, protocols, LAN vs WAN |
| 02 | [OSI Model](networking/notes/02-osi-model.md) | 7-layer model mapped to real DevOps troubleshooting |
| 03 | [DNS](networking/notes/03-dns.md) | Record types, resolution flow, propagation |
| 04 | [Routing](networking/notes/04-routing.md) | Routing tables, gateways, static vs dynamic, BGP/OSPF |
| 05 | [Subnetting](networking/notes/05-subnetting.md) | CIDR, VPC subnet design, NAT |
| 06 | [Troubleshooting](networking/notes/06-troubleshooting.md) | A layer-by-layer diagnostic framework |
| 07 | [Commands](networking/notes/07-commands.md) | Linux, networking, Git, and SSH/EC2 command reference |

### 📁 Structure

```
devops-learning-networking/
├── README.md
└── networking/
    ├── diagrams/
    │   ├── osi-model.svg
    │   └── subnetting-cidr.svg
    └── notes/
        ├── 01-fundamentals.md
        ├── 02-osi-model.md
        ├── 03-dns.md
        ├── 04-routing.md
        ├── 05-subnetting.md
        ├── 06-troubleshooting.md
        └── 07-commands.md
```

### 🎯 Why This Exists

- A quick-reference I can return to whenever networking questions come up in real work
- A way to connect theory (OSI, CIDR, DNS) directly to the tools used to observe and debug it (`dig`, `traceroute`, `nc`, `ip route`)
- A portfolio piece that shows networking fundamentals are solid going into cloud and Kubernetes networking

### 🧠 What's Covered

**Fundamentals** — IP, MAC, packets, ports, protocols, LAN/WAN, NAT, DHCP

**OSI Model** — the 7 layers explained with the commands that map to each one

**DNS** — A/AAAA/CNAME/MX/TXT records, the resolution path from browser to nameserver, propagation

**Routing** — routing tables, gateways, `traceroute`, static vs dynamic routing, BGP/OSPF

**Subnetting** — CIDR notation, VPC subnet design, public/private/database subnet separation, NAT gateways

**Troubleshooting** — a layer-by-layer method for isolating whether an issue is connectivity, DNS, routing, ports, or the application itself

**Commands** — the Linux, networking, Git, and SSH/EC2 commands used throughout the above

### 🛠️ Tools Used

VS Code · Git & GitHub · Linux · AWS EC2 · Terminal

### 📄 License

MIT — feel free to use or adapt.
