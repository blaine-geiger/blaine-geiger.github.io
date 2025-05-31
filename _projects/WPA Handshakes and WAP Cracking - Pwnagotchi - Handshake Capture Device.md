---
title: WPA Handshakes and WAP Cracking
date: 2024-05-04 08:01:35 +0300
#subtitle: Hashcat, Bettercap, Wordlists
image: '/images/finished_build.jpg'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
github_url: https://github.com/blaine-geiger/Pwnagotchi
---

---

<a href="{{ page.github_url }}" target="_blank" style="text-decoration: none;">
  <img src="https://img.shields.io/badge/View%20The%20Details%20on-GitHub-181717?style=for-the-badge&logo=github" alt="View the full project on GitHub">
</a>

####  **Goals**
- Build a portable, automated WPA handshake capturing device for educational and ethical security testing.
- Learn how to assemble and configure a custom headless device using **Bettercap**, **Raspberry Pi Zero**, and an **eInk display**.
- Leverage AI-driven behavior to optimize wireless packet capture strategies.

---

####  **Tools & Technologies**
- **Hardware**:
  - Raspberry Pi Zero WH (2.4GHz Wi-Fi)
  - Waveshare 2.13" eInk display (V4)
  - PiSugar 2 1200mAh battery pack
  - 3D printed case
- **Software**:
  - Pwnagotchi OS (custom Linux image)
  - Bettercap (for Wi-Fi deauthentication and packet capture)
  - Web UI for configuration and monitoring
  - Configuration via `config.toml` file

---

####  **Methods / Architecture**
- Flashed Pwnagotchi image to SD card via **Raspberry Pi Imager**
- Configured device static IP (e.g., `10.0.0.1/24`) and SSH credentials
- Edited `config.toml` to set:
  - Device name
  - Display type
  - Whitelist for safe WAPs
  - Plugins and behavior customization
- Accessed **Web UI** and **Bettercap GUI** over local IP for live stats and control
- Employed reinforcement learning (built-in) to improve packet capture strategy over time
- Operated in fully **headless mode** with Bluetooth tethering for mobile monitoring

---

####  **Skills Demonstrated**
- Wireless security testing and WPA handshake collection
- Embedded Linux configuration and device setup
- Safe use of **deauthentication attacks** in lab conditions
- Understanding of **Bettercap’s** role in network-level attacks
- Customizing Linux-based embedded systems and secure SSH access
- Integration of lightweight UIs for remote device management

---

####  **Photos**
![Battery, Pi Zero, and eInk Display](/images/parts_together.jpg)
![Components inside casing](/images/parts_in_case.jpg)
![Finished build](/images/finished_build.jpg)

---
<br>
<br>