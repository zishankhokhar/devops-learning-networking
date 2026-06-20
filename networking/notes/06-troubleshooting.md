## Networking Troubleshooting

### 🧩 Why Troubleshooting Matters
In DevOps, most outages come down to networking issues.
Troubleshooting helps you answer:
- Is the server reachable?
- Is DNS resolving correctly?
- Is the port open?
- Is the application responding?
- Is routing correct?
A good engineer doesn’t guess — they test.

### 🔍 Troubleshooting Framework (The 5‑Layer Method)
1. Check Physical / Connectivity
- Is the machine online?
- Is the network interface up?
Commands:
ping 8.8.8.8
ip addr

2. Check DNS
If DNS is broken, nothing loads.
Commands:
nslookup example.com
dig example.com
dig example.com +trace

3. Check Routing
Make sure packets know where to go.
Commands:
ip route
traceroute google.com

4. Check Ports
Is the service listening?
Is the firewall blocking it?
Check open ports:
sudo netstat -tulpn
Check if a port is reachable:
nc -zv example.com 80

5. Check Application Layer
If networking is fine, check the app.
Commands:
curl -I http://example.com
curl -v http://example.com

### 🛠️ Common Issues & Fixes
❌ Issue: DNS not resolving
Cause: Wrong nameserver or missing A record
Fix: Update DNS records and wait for propagation

❌ Issue: EC2 not reachable
Cause: Security group blocking traffic
Fix: Allow inbound port 80 or 22

❌ Issue: NGINX not loading
Cause: Service not running
Fix:
sudo systemctl status nginx
sudo systemctl restart nginx

❌ Issue: Wrong routing
Cause: Missing default gateway
Fix: Check routing table:
ip route

### 🧪 Useful Commands Summary
Code
ping google.com
nslookup domain.com
dig domain.com
traceroute google.com
curl -I http://example.com
nc -zv example.com 80
ip route
ip addr

### 💡 What Finally Clicked
Troubleshooting is just elimination:
- If ping works → network is fine
- If DNS works → name resolution is fine
- If traceroute works → routing is fine
- If port is open → firewall is fine
- If curl works → application is fine
You move from bottom → top, just like the OSI model.