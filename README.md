# Splunk Dashboard on AWS EC2 (RHEL)

This project demonstrates how to install Splunk on an AWS EC2 instance running Red Hat (RHEL), configure it, and create a beginner-friendly dashboard with multiple visualizations.

---

## 🚀 Setup Steps

### 1. Launch EC2
- Instance Type: `t2.medium` (2 vCPU, 4 GB RAM)
- Storage: At least **20 GB** recommended
- Security Group: Allow inbound on port **8000**

### 2. Install Splunk
Run the commands from:
```bash
setup/splunk_install_rhel.sh

**3. Start Splunk**
sudo /opt/splunk/bin/splunk start --accept-license

Login at:
http://<EC2-Public-IP>:8000
