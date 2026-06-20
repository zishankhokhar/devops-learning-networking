## Commands
A practical collection of essential Linux, networking, Git, and troubleshooting commands used throughout DevOps work.
This hybrid version gives you quick reference + deeper explanations where useful.

### 🧠 Key Concepts
- Linux commands help you navigate, manage files, and control the system
- Networking commands help you test connectivity, DNS, routing, and ports
- Git commands help you track and push your work
- EC2/SSH commands help you connect to cloud servers
- Troubleshooting commands help you diagnose issues layer‑by‑layer

### 📘 Deep Dive Into Command Categories
Below are the most important command groups you’ll use daily as a DevOps engineer.

### 📁 File & Directory Commands
pwd                     # show current directory
ls                      # list files and folders
ls -la                  # list all files with details
cd <dir>                # change directory
mkdir <name>            # create a directory
touch <file>            # create an empty file
cp <src> <dest>         # copy files
mv <src> <dest>         # move or rename files
rm <file>               # delete a file
rm -r <dir>             # delete a folder and its contents
Why it matters:  
You’ll constantly navigate servers, edit configs, and manage deployments.

### 📄 Viewing & Editing Files
cat <file>              # print file contents
less <file>             # view file page by page
head <file>             # first 10 lines
tail <file>             # last 10 lines
tail -f <file>          # live log monitoring
nano <file>             # simple text editor
vim <file>              # advanced editor
DevOps example:  
Checking NGINX logs:
tail -f /var/log/nginx/access.log

### 🔐 Permissions & Ownership
chmod 755 <file>        # change permissions
chmod 400 <key.pem>     # required for SSH keys
chown user:group <file> # change owner
Why it matters:  
Incorrect permissions break deployments, SSH access, and services.

### 🧩 Process & Service Management
ps aux                  # list running processes
top                     # live process monitor
systemctl status <svc>  # check service status
systemctl restart <svc> # restart a service
systemctl enable <svc>  # start service on boot
kill <PID>              # stop a process
kill -9 <PID>           # force stop
DevOps example:  
Restarting NGINX after config changes:
sudo systemctl restart nginx

### 🌐 Networking Commands
ip addr                 # show IP addresses
ip route                # show routing table
ping <host>             # test connectivity
traceroute <host>       # trace packet path
nslookup <domain>       # DNS lookup
dig <domain>            # detailed DNS lookup
curl -I <url>           # fetch headers
curl -v <url>           # verbose request
nc -zv <host> <port>    # check if port is open
Why it matters:  
These commands map directly to OSI troubleshooting layers.

### 🧪 Practical Networking Examples
Check if DNS works:
dig google.com

Check if port 80 is open:
nc -zv example.com 80

Check routing:
traceroute google.com

### 🔑 SSH & EC2 Commands
chmod 400 <key.pem>                       # fix key permissions
ssh -i <key.pem> ec2-user@<PUBLIC_IP>     # connect to EC2
scp -i <key.pem> file.txt ec2-user@<IP>:/home/ec2-user/   # upload file
Why it matters:  
SSH is how you access cloud servers for deployments and debugging.

### 🧰 Git Commands
git init
git status
git add .
git commit -m "message"
git push
git pull
git branch
git checkout -b <branch>

DevOps example:  
Pushing your notes:
git add .
git commit -m "Add networking notes"
git push

### 🧹 Useful Shortcuts
Tab        # auto-complete
Ctrl + C   # stop a running command
Ctrl + L   # clear terminal
Ctrl + A   # go to start of line
Ctrl + E   # go to end of line

### 🛠️ Troubleshooting Tips
- If SSH fails → check key permissions
- If website fails → test port 80 with nc
- If DNS fails → test with dig
- If routing fails → use traceroute
- If service fails → check logs with journalctl

### 📝 Summary
This command set forms your daily DevOps toolkit.
You’ll use these commands across Linux servers, EC2 instances, deployments, debugging sessions, and automation scripts.