# CYBERSECURITY-TASK-4
# Task 4 – Firewall Configuration using UFW

## 📌 Objective
Configure and test firewall rules on Linux using UFW (Uncomplicated Firewall) to allow and block network traffic.

---

## 🖥 System Used
- Kali Linux  
- UFW (Uncomplicated Firewall)

---

## 📸 Evidence
All firewall configuration and testing were performed in a single terminal session.  
One screenshot containing all commands and outputs is stored inside the screenshots folder.

---

## 🛠 Firewall Commands and Their Purpose

| Command | Description |
|--------|-------------|
| sudo ufw enable | Enables the firewall and starts filtering network traffic |
| sudo ufw status | Displays the current firewall rules |
| sudo ufw deny 23 | Blocks all inbound traffic on port 23 (Telnet) |
| sudo ufw allow 22 | Allows inbound traffic on port 22 (SSH) |
| sudo ufw status verbose | Shows detailed firewall rules and policies |
| nc -zv 127.0.0.1 23 | Tests whether Telnet port (23) is blocked |
| nc -zv 127.0.0.1 22 | Tests whether SSH port (22) is allowed |
| sudo ufw delete deny 23 | Removes the Telnet blocking rule |

---

## 🔐 Why Port 23 (Telnet) Was Blocked
Telnet transmits usernames and passwords in plain text, making it insecure. Blocking this port helps prevent attackers from intercepting sensitive information.

---

## 🔑 Why Port 22 (SSH) Was Allowed
SSH uses encryption for secure remote access. Allowing this port enables safe system administration.

---

## ✅ Result
The firewall successfully blocked Telnet (port 23) and allowed SSH (port 22).  
Port testing using Netcat confirmed that the firewall rules were working correctly.

---

## 🧠 Conclusion
This task demonstrated how firewall rules control network traffic. By blocking insecure services and allowing secure ones, UFW provides effective protection against unauthorized access and cyber threats.
