# SOC-Automation-Lab
## Setup

### **Step 1: Download Windows ISO**
Download the Windows ISO from Microsoft:
```bash
https://www.microsoft.com/en-in/software-download/windows11
```
Mount the ISO in VMware Workstation Pro and complete the installation.

### Step 2: Configure Windows VM
- Create a new VM in VMware
- Attach the ISO
- Install Windows
- Complete setup and ensure network connectivity

### Step 3: Install Sysmon
Download Sysmon: 
```bash
https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon
```
### Sysmon Configuration
- After downloading Sysmon, extract the ```bash .zip``` file.
- Open the extracted Sysmon folder.
- Download the Sysmon configuration file: ```bash https://github.com/olafhartong/sysmon-modular/blob/master/sysmonconfig.xml```
- Click on Raw
- Right-click → ***Save As***
- Save it as ```bash sysmonconfig.xml``` inside the Sysmon folder
- This configuration enables advanced logging rules for better threat visibility.

### Cloud Infrastructure Setup
- For this lab, cloud VMs are used to host core SOC components.
- I used Vultr, but you can use AWS, Azure, or any cloud provider.
- ```bash https://console.vultr.com/ ```

**A) VM 1: Wazuh Server (SIEM)**
- CPU: 4 vCPU
- RAM: 8 GB
- Storage: 160 GB SSD
- OS: Ubuntu 24.04 x64
- Backups: Disabled

**B) VM 2: TheHive Server (Case Management)**
- CPU: 6 vCPU
- RAM: 16 GB
- Storage: 320 GB SSD
- OS: Ubuntu 24.04 x64
- Backups: Disabled

These VMs form the backbone of the SOC lab, handling **log analysis, alerting, and incident response workflows.**



