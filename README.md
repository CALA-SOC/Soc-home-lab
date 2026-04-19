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

**VM Setup**
📸 *![VM Setup](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/VMs%20Setup.png)*

---

## 🌐 Network Configuration

All virtual machines are connected using an **Internal Network** in VirtualBox to simulate a controlled enterprise environment.

* Ensures isolated communication between VMs
* Prevents interference with external networks

**VM Network Setup**
📸 *![Network Setup](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Network%20Configuration.png)*

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

---

### 2. Network Configuration

* Configured all VMs to use **Internal Network**
* Verified connectivity using ping between systems

**Connectivity Verification**
📸 *![Connectivity Verification](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Sucessful%20ping%20between%20VM's.png)*

---

### 3. Active Directory Setup (Windows Server)

* Installed Active Directory Domain Services (AD DS)
* Promoted server to Domain Controller
* Created a domain

**AD DS to Domain Controller**
📸 *![AD DS installation](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/AD%20DS%20to%20Domain%20controller.png)*

---

### 4. Domain Integration

* Joined Windows Client VM to the domain
* Verified domain authentication

**Joining domain**
📸 *![Joining domain](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Sucessful%20domain%20joning.png)*

**Successful domain login**
📸 *![Successful domain login](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Domian%20Login.png)*

---

### 5. Sysmon Installation

* Installed Sysmon on:

  * Windows Client VM
  * Windows Server VM
* Configured logging for system activity monitoring

**Sysmon installation command**
📸 *![Sysmon installation command](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Sysmon%20Installation%20command.png)*

**Sysmon logs in Event Viewer**
📸 *![Sysmon logs in Event Viewer](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Sysmon%20Logs%20in%20Event%20viewer.png)*

---

### 6. Splunk Setup

* Installed Splunk Enterprise on Splunk VM
* Configured web interface and initial setup

**Splunk Installation**
📸*![Splunk Installation](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Splunk%20Installation.png)

**Splunk Dashboard**
📸 *![Splunk dashboard](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/Splunk%20dashboard.png)*

---

### 7. Splunk Universal Forwarder Configuration

* Installed on:

  * Windows Client VM
  * Windows Server VM
* Configured to send logs to the Splunk server

**inputs.conf configuration file**
📸 *![inputs.conf configuration](https://github.com/CALA-SOC/Soc-home-lab/blob/main/Screenshots/inputs.conf%20file_M.png)*

---

### 8. Log Ingestion & Monitoring

* Verified logs are being received in Splunk
* Created basic searches and queries

Example:

* Login events
* Sysmon activity logs

**Logs in Splunk search**
📸 *Insert Screenshot Here: Logs in Splunk search*

---

## 🔍 Use Cases Simulated

* Endpoint monitoring using Sysmon
* Centralized log collection
* Domain-based authentication logging

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

