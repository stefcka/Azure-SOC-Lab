# Azure-SOC-Lab
Expanding my Azure knowledge, I created a virtual machine vulnerable to the internet...this is how it went.

STAGE 1 | Configuring Virtual Machine
- In Azure I learned the proper way to set a virtual machine, analyze the best regions to configure the VM and troubleshot through Azure cloud shell during region pairing issues.
- I learned that port 3389 allows all IP addresses, from any source to access my virtual machine
- Set up inbound security rules, and made my VM public

  
- Accessed my virtual machine through remote desktop connection, turned off window defender firewall protection to _____, and explored ways to read logs.

  
- Created a log analytics workspace where I learned how to query using KQL to reach different data about my VM.
- Set up a Sentinel instance to integrate with logs.
- Designed custom KQL detection rules in Microsoft Sentinel to detect RDP brute-force and password-spraying attacks against exposed endpoints.
- Parsed Windows SecurityEvent 4625 logs, enriching raw attacker IP data with geolocation metadata to map global threat vectors.
- Built interactive Microsoft Sentinel Workbooks displaying live threat maps and attack trends to streamline incident triage.

