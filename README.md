# FIREWALL_on_linux
# 🔥 Task 4: Setup and Use a Firewall (UFW - Linux)

### 🧠 Cyber Security Internship – Task 4.3

---

## 🎯 Objective
To configure and test basic firewall rules using **UFW (Uncomplicated Firewall)** on Linux for allowing and blocking specific ports.

---

## 🧰 Tools & Environment
- **Operating System:** Kali Linux  
- **Firewall Tool:** UFW (Uncomplicated Firewall)  
- **Utility for Testing:** Netcat (`nc`)  
- **Terminal:** Zsh / Bash  

---

## 🪜 Steps Performed

```bash
1️⃣ Enable UFW
sudo ufw enable
✅ Output: Status: active
This confirms the firewall is now running.

2️⃣ List Existing Rules
sudo ufw status numbered

3️⃣ Block Inbound Traffic on Port 23 (Telnet)
sudo ufw deny 23
sudo ufw status numbered


📸 Screenshot 1: Shows port 23 DENY Anywhere

4️⃣ Test the Rule (Telnet Block)

Install netcat if not present:

sudo apt install netcat-traditional -y


Test connection:

nc -zv localhost 23


🧩 Expected Output:

nc: connect to localhost port 23 (tcp) failed: Connection refused


📸 Screenshot 2: Telnet connection refused – rule verified.
5️⃣ Allow SSH (Port 22)
sudo ufw allow 22
sudo ufw status numbered


✅ SSH is now explicitly allowed.
