📊 Elastic SIEM Lab using Kali Linux
🔍 Overview
This project demonstrates the setup and configuration of Elastic SIEM on Elastic Cloud to collect and analyze security events generated from a Kali Linux virtual machine. The lab uses Elastic Agent for log forwarding and Nmap to generate security events for analysis.

⚙️ Technologies Used
Elastic SIEM (Elastic Cloud & Kibana)
Kali Linux (Virtual Machine using Oracle VirtualBox)
Elastic Agent (for log collection)
Nmap (Network scanning tool for generating security events)
🚀 Setup Instructions
1️⃣ Set Up Elastic Cloud SIEM
Create a free Elastic Cloud account: Elastic Cloud
Deploy Elasticsearch and Kibana by following the default deployment instructions.
2️⃣ Set Up Kali Linux VM
Download Kali Linux VM: Get Kali Linux
Import the VM into Oracle VirtualBox or VMware and complete the installation.
Default Kali credentials:
plaintext
Copy
Edit
Username: kali
Password: kali
3️⃣ Install and Configure Elastic Agent
In Kibana, navigate to Integrations → Elastic Defend and install it.
Copy the provided installation command and run it in Kali’s terminal:
bash
Copy
Edit
sudo ./elastic-agent install --url=<elastic-url> --enrollment-token=<token>
Verify the agent status:
bash
Copy
Edit
sudo systemctl status elastic-agent.service
4️⃣ Generate Security Events Using Nmap
Ensure Nmap is installed (pre-installed on Kali).
Run various Nmap scans to generate logs:
bash
Copy
Edit
sudo nmap <vm-ip>
sudo nmap -sS <ip-address>
sudo nmap -p- <ip-address>
Check Elastic SIEM for detected security events and logs.
📈 Project Outcomes
✅ Elastic SIEM successfully deployed on Elastic Cloud.
✅ Logs collected from Kali Linux VM using Elastic Agent.
✅ Security events generated and visualized using Nmap scans in SIEM dashboards.
💡 Key Learnings
Real-time threat detection using Elastic SIEM.
Log collection and forwarding using Elastic Agent.
Network scanning and security event generation using Nmap.
