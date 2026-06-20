## OSI Model

### 🧱 What the OSI Model Is
The OSI Model (Open Systems Interconnection) is a 7‑layer framework that explains how data moves across a network.
It helps engineers understand where a problem is happening and how communication flows.
It’s a mental model — not something physically implemented — but it’s extremely useful in DevOps.

### 🧩 The 7 Layers of the OSI Model
1. Physical Layer
Handles physical connections: cables, signals, voltages, Wi‑Fi radio waves.
Examples: Ethernet cables, fibre optics.

2. Data Link Layer
Responsible for MAC addresses and switching.
Breaks data into frames.
Examples: Switches, ARP.

3. Network Layer
Handles IP addresses and routing.
Moves packets between networks.
Examples: Routers, IPv4, IPv6.

4. Transport Layer
Provides end‑to‑end communication.
Uses ports and protocols.
Examples: TCP, UDP, port numbers.

5. Session Layer
Manages sessions between devices.
Examples: API sessions, authentication sessions.

6. Presentation Layer
Formats and encrypts data.
Examples: SSL/TLS, compression, encoding.

7. Application Layer
Where users and applications interact.
Examples: HTTP, DNS, SSH, SMTP.

### 🧠 Why the OSI Model Matters in DevOps
- Helps troubleshoot network issues
- Helps understand where packets are failing
- Helps explain how cloud services communicate
- Helps understand firewalls, load balancers, and routing
- Helps debug Kubernetes networking
When something breaks, you can ask:
“Which layer is failing?”

### 🔍 OSI Model from Sender & Receiver POV
When sending data:
- Starts at Layer 7 → Layer 1  
        When receiving data:
- Goes Layer 1 → Layer 7
This is called encapsulation and decapsulation.

### 🛠️ Useful Commands (Mapped to Layers)
Layer 3 – Network
ping google.com

Layer 4 – Transport
nc -zv example.com 80

Layer 7 – Application
curl -I http://example.com

### 💡 What Finally Clicked
The OSI model is just a way to break down communication into steps:
- Layers 1–3 → network infrastructure
- Layers 4–7 → applications and data
Once you understand this, debugging becomes much easier.