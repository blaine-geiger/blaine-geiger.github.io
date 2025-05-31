---
title: Bash Scripting - automating `airmon-ng`
date: 2024-05-04 08:01:35 +0300
#subtitle: Scripting, Automation
image: '/images/script_run.png'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
github_url: https://github.com/blaine-geiger/automate-airmon
---

---

<a href="{{ page.github_url }}" target="_blank" style="text-decoration: none;">
  <img src="https://img.shields.io/badge/View%20The%20Details%20on-GitHub-181717?style=for-the-badge&logo=github" alt="View the full project on GitHub">
</a>

####  **Goals**
- Simplify and automate the process of configuring a Wi-Fi adapter for monitor mode using `airmon-ng`.
- Reduce manual steps and potential errors during wireless auditing setups.
- Enhance efficiency for ethical hacking and penetration testing workflows.

---

####  **Tools & Technologies**
- **Operating System**: Kali Linux
- **Scripting Language**: Bash
- **Utilities**:
  - `airmon-ng` – for enabling monitor mode
  - `airodump-ng` – for passive Wi-Fi traffic capture
  - `macchanger` – for MAC address spoofing

---

####  **Methods / Architecture**
- **Interface Detection**: Script identifies all available wireless interfaces.
- **User Interaction**: Prompts user to select the desired interface for monitor mode.
- **Process Management**: Terminates processes that may interfere with monitor mode.
- **MAC Address Spoofing**: Randomizes the MAC address of the selected interface for anonymity.
- **Monitor Mode Activation**: Enables monitor mode on the chosen interface.
- **Verification**: Confirms that the interface is successfully in monitor mode.
- **Traffic Capture**: Offers the option to initiate `airodump-ng` for passive traffic monitoring.

---

####  **Skills Demonstrated**
- Bash scripting for automation of network interface configurations.
- Integration of multiple command-line tools to streamline workflows.
- Understanding of wireless interface management and security considerations.
- Enhancing operational efficiency in penetration testing environments.

---

####  **Screenshots**
![Automate Airmon Script Execution](/images/script_run.png)