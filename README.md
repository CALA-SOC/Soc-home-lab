# SOC Home Lab Project (VirtualBox + Splunk + Active Directory)

## 📌 Overview

This project demonstrates the design and implementation of a **Security Operations Center (SOC) home lab** using VirtualBox. The lab simulates a real-world enterprise environment where security monitoring, log collection, and attack detection can be performed.

The setup includes multiple virtual machines configured for:

* Attack simulation
* Endpoint monitoring
* Domain control (Active Directory)
* Centralized logging (Splunk)

---

## 🏗️ Lab Architecture

The lab consists of four virtual machines:

1. **Linux VM**

   * Used for simulating attacks (e.g., SSH brute force, scanning, etc.)

2. **Windows Client VM**

   * Simulates an endpoint user system
   * Configured with Sysmon and Splunk Universal Forwarder

3. **Windows Server VM**

   * Configured as Domain Controller (Active Directory)
   * Central authentication and logging point
   * Also installed with Sysmon and Splunk Forwarder

4. **Splunk VM**

   * Central log collection and analysis system
   * Receives logs from Windows systems

📸 *Insert Screenshot Here: Overall VM setup in VirtualBox*

---

## 🌐 Network Configuration

All virtual machines are connected using an **Internal Network** in VirtualBox to simulate a controlled enterprise environment.

* Ensures isolated communication between VMs
* Prevents interference with external networks

📸 *Insert Screenshot Here: VirtualBox network settings*

---

## ⚙️ Tools & Technologies Used

* VirtualBox
* Windows Server (Active Directory)
* Windows 10/11 Client
* Linux (Attack Machine)
* Sysmon (System Monitoring)
* Splunk Enterprise
* Splunk Universal Forwarder

---

## 🛠️ Implementation Steps

### 1. Virtual Machine Setup

* Installed and configured 4 virtual machines
* Allocated system resources (RAM, CPU, storage)
* Installed operating systems

📸 *Insert Screenshot Here: VM creation process*

---

### 2. Network Configuration

* Configured all VMs to use **Internal Network**
* Verified connectivity using ping between systems

📸 *Insert Screenshot Here: Successful ping between VMs*

---

### 3. Active Directory Setup (Windows Server)

* Installed Active Directory Domain Services (AD DS)
* Promoted server to Domain Controller
* Created a domain

📸 *Insert Screenshot Here: AD DS installation*
📸 *Insert Screenshot Here: Domain creation confirmation*

---

### 4. Domain Integration

* Joined Windows Client VM to the domain
* Verified domain authentication

📸 *Insert Screenshot Here: Joining domain*
📸 *Insert Screenshot Here: Successful domain login*

---

### 5. Sysmon Installation

* Installed Sysmon on:

  * Windows Client VM
  * Windows Server VM
* Configured logging for system activity monitoring

📸 *Insert Screenshot Here: Sysmon installation command*
📸 *Insert Screenshot Here: Sysmon logs in Event Viewer*

---

### 6. Splunk Setup

* Installed Splunk Enterprise on Splunk VM
* Configured web interface and initial setup

📸 *Insert Screenshot Here: Splunk dashboard*

---

### 7. Splunk Universal Forwarder Configuration

* Installed on:

  * Windows Client VM
  * Windows Server VM
* Configured to send logs to Splunk server

📸 *Insert Screenshot Here: Forwarder installation*
📸 *Insert Screenshot Here: inputs.conf configuration*

---

### 8. Log Ingestion & Monitoring

* Verified logs are being received in Splunk
* Created basic searches and queries

Example:

* Login events
* Sysmon activity logs

📸 *Insert Screenshot Here: Logs in Splunk search*

---

## 🔍 Use Cases Simulated

* Endpoint monitoring using Sysmon
* Centralized log collection
* Domain-based authentication logging
* Attack simulation from Linux machine
* Detection of suspicious activities

---

## 📊 Key Skills Demonstrated

* SOC environment setup
* Log analysis using Splunk
* Active Directory administration
* Endpoint monitoring (Sysmon)
* Network configuration in VirtualBox
* Security event detection

---

## 🚀 Future Improvements

* Integrate SIEM use cases and alerts
* Add Sigma rules for detection
* Simulate real-world attack scenarios (MITRE ATT&CK)
* Implement dashboards in Splunk
* Add automated alerting

---

## 📁 Project Structure

```
SOC-Home-Lab/
│
├── README.md
├── screenshots/
│   ├── vm-setup.png
│   ├── network-config.png
│   ├── ad-setup.png
│   ├── sysmon-install.png
│   ├── splunk-dashboard.png
│   └── logs.png
└── configs/
    ├── sysmon-config.xml
    └── inputs.conf
```

---

## 📌 Conclusion

This project showcases a practical implementation of a SOC environment, demonstrating the ability to build, configure, and monitor systems in a simulated enterprise network.

It highlights hands-on experience in cybersecurity operations, making it suitable for entry-level SOC Analyst roles.

---
