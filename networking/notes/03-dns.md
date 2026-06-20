## DNS (Domain Name System)

### 🌐 What DNS Is
DNS is the system that converts human‑friendly domain names into machine‑friendly IP addresses.

Example:
google.com → 142.250.187.206

Without DNS, we would have to type IP addresses into browsers.

### 🧠 Why DNS Matters in DevOps
DNS is everywhere in cloud engineering:
- EC2 instances need DNS to map domains to public IPs
- Load balancers use DNS names
- Kubernetes uses internal DNS for service discovery
- Certificates (SSL/TLS) rely on DNS validation
- Troubleshooting often starts with DNS checks
If DNS breaks, nothing loads.

### 🧩 DNS Components
1. Nameservers
Servers responsible for storing DNS records for a domain.
Examples: Cloudflare, Route53.

2. Zone File
A file that contains all DNS records for a domain.

3. DNS Records
Instructions that tell DNS how to route traffic.

### 📘 Common DNS Record Types
A Record
Maps a domain → IPv4 address.
Example:
example.com → 3.88.120.55

AAAA Record
Maps a domain → IPv6 address.

CNAME Record
Alias for another domain.
Example:
www.example.com → example.com

MX Record
Mail server settings.

TXT Record
Used for verification (Google, AWS, email security).

### 🔄 How DNS Works (Step-by-Step)
1. User types a domain into the browser
2. Browser checks local DNS cache
3. If not found → asks DNS resolver (ISP or Cloudflare)
4. Resolver queries the domain’s nameserver
5. Nameserver returns the IP address
6. Browser connects to the server using that IP
This entire process usually takes milliseconds.

### 🛠️ DNS Debugging Tools
nslookup
Basic DNS lookup tool.
nslookup google.com

dig
More detailed DNS query tool.
dig google.com

Check DNS propagation
Useful when you update A records.
dig yourdomain.com +trace

/etc/hosts
Local override file for testing.
sudo nano /etc/hosts

### 🧪 Useful Examples
Check A record
dig A example.com

Check nameservers
dig NS example.com

Check CNAME
dig CNAME www.example.com

### 💡 What Finally Clicked
DNS is basically the phonebook of the internet:
- Domain name = person’s name
- IP address = phone number
- DNS resolver = directory service
- Nameserver = where the records are stored
When you update DNS (like pointing your domain to EC2), it takes time to propagate globally — this is why sometimes your domain doesn’t work immediately.