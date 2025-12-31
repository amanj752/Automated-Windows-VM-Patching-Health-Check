# Automated Windows VM Patching & Health Check

## 📌 Overview

This open-source project automates **Windows Virtual Machine patching and health checks** using **Ansible and PowerShell**. It is designed for cloud and infrastructure engineers who manage Windows servers, domain controllers, and VM-based environments.

The solution performs **pre-patch health checks**, installs Windows updates, manages reboots safely, and generates a **patch compliance report**.

---

## 🎯 Objectives

* Automate Windows Server patching
* Reduce manual effort and patching errors
* Ensure server health before and after patching
* Support VM-based environments (On‑prem / Cloud)

---

## 🧩 Key Features

* ✅ Disk space check before patching
* ✅ Last reboot time validation
* ✅ Windows Update installation
* ✅ Safe reboot handling
* ✅ Service health validation (DNS, AD, etc.)
* ✅ Patch execution report (CSV / TXT)

---

## 🛠️ Technology Stack

* **Ansible** – Automation framework
* **PowerShell** – Windows health checks
* **WinRM** – Windows remote management
* **Windows Server 2016+**

---

## 📁 Project Structure

```
windows-vm-patching/
│
├── inventory/
│   └── windows_hosts.ini
│
├── playbooks/
│   ├── health_check.yml
│   ├── patching.yml
│   └── reboot.yml
│
├── roles/
│   ├── health_check/
│   ├── windows_update/
│   └── reboot_control/
│
├── scripts/
│   └── disk_service_check.ps1
│
└── README.md
```

---

## ⚙️ Prerequisites

* Ansible installed on control node
* WinRM enabled on Windows VMs
* PowerShell 5.1 or later
* Administrator access on target servers

---

## 🚀 How It Works

1. Ansible connects to Windows VMs via WinRM
2. Health checks are performed using PowerShell
3. Windows Updates are installed
4. System reboots if required
5. Post-patch validation is performed
6. Patch status report is generated

---

## ▶️ Usage

### Run Health Check

```bash
ansible-playbook playbooks/health_check.yml
```

### Run Windows Patching

```bash
ansible-playbook playbooks/patching.yml
```

### Reboot Handling

```bash
ansible-playbook playbooks/reboot.yml
```

---

## 📊 Sample Report Output

* Server Name
* Last Reboot Time
* Disk Space Status
* Patch Status
* Reboot Required (Yes/No)

---

## 🔐 Best Practices Implemented

* No simultaneous reboot of critical servers
* Pre and post patch validation
* Modular Ansible roles

---

## 📈 Future Enhancements

* Azure VM tag-based patching
* Domain Controller safe patching logic
* Email / Teams notification
* Prometheus metrics exporter

---

## 👨‍💻 Ideal For

* Cloud Infrastructure Engineers
* Windows Server Administrators
* NOC / Operations Teams
* Patch & Vulnerability Management

---

## 📄 License

This project is released under the **MIT License**.

---

## 🤝 Contributions

Contributions, issues, and feature requests are welcome.

---

## ⭐ Why This Project Matters

This project reflects **real-world enterprise patching workflows** and demonstrates hands-on experience in automation, Windows infrastructure, and operational reliability.
