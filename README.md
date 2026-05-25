# SSH Brute Force Investigation (Kali Linux Lab)

##  Overview
This project simulates and investigates an SSH brute-force attack in a controlled Linux environment using Kali Linux. The goal is to understand how authentication attacks work and how to analyze system logs from a security (SOC) perspective.

---

##  Objectives
- Simulate SSH brute-force attack
- Generate real authentication logs
- Analyze failed login attempts
- Identify attacker activity
- Practice basic SOC / incident response workflow

---

## Tools Used
- Kali Linux
- OpenSSH (SSH server)
- Hydra
- journalctl (system logs)
- Linux CLI tools: grep, awk, wc

---

##  Attack Simulation

A brute-force attack was performed using Hydra against a local SSH service:

```bash
hydra -t 4 -l root -P /usr/share/wordlists/rockyou.txt ssh://127.0.0.1
