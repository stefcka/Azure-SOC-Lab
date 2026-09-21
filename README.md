# Azure-SOC-Lab
Expanding my Azure knowledge, I created a virtual machine vulnerable to the internet...this is how it went.

Languaged Used
-KQL
-Powershell
-Azure Cloudshell

STAGE 1 | Configuring Virtual Machine
- In Azure I learned the proper way to set a virtual machine, analyze the best regions to configure the VM based on pricing, and troubleshot through Azure cloud shell during region pairing issues.
- I learned that port 3389 allows all IP addresses, from any source to access my virtual machine
  <img width="1903" height="520" alt="Screenshot 2026-09-21 090419" src="https://github.com/user-attachments/assets/1af87e7f-8895-41fd-a57a-28dc3f80be0e" />
- Set up inbound security rules, and made my VM public
- Accessed my virtual machine through remote desktop connection, turned off window defender firewall protection to stop blocking unsolicited incoming network traffic, and explored ways to read logs.
<img width="1745" height="927" alt="Screenshot 2026-09-20 235125" src="https://github.com/user-attachments/assets/73ddf7e9-0d6a-4a88-8ba1-92ea34b0cc74" />

STAGE 2 | Analyzing logs + KQL 
- Created a log analytics workspace where I learned how to query using KQL to reach different data about my VM.
- Set up a Sentinel instance to integrate with logs.
- Designed custom KQL detection rules in Microsoft Sentinel to detect RDP brute-force and password-spraying attacks against exposed endpoints.
- Parsed Windows SecurityEvent 4625 logs, enriching raw attacker IP data with geolocation metadata to map global threat locations.
<img width="1919" height="872" alt="Screenshot 2026-09-20 160641" src="https://github.com/user-attachments/assets/74f35c03-75ee-4f97-8d5c-7ab1a2a5f632" />
- Built interactive Microsoft Sentinel Workbooks displaying live threat maps and attack trends, analyzing hotspots for threats.
<img width="1604" height="703" alt="Screenshot 2026-09-21 084912" src="https://github.com/user-attachments/assets/fa5174ac-ab0a-47c3-80cb-454977b63c41" />
  (France having the highest amount of failed login attempts can be due to the low cost of hosting servers. Hence why cybercriminals tend to build their botnets in hubs like France.)


