---
title: USB Wi-Fi Antennas for Monitor Mode and Packet Injection
date: 2024-05-04 08:01:35 +0300
#subtitle: Monitor Mode, Linux Drivers, 
image: '/images/ACS_036.jpg'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
---

####  **Goals**
- Set up the Alfa AWUS036ACS (Realtek RTL8811AU chipset) on Kali Linux with full support for monitor mode and packet injection.
- Test compatibility across kernel versions using DKMS-backed driver installation.
- Integrate the adapter into a Wi-Fi auditing toolkit for lab-based security testing.

---

####  **Tools & Technologies**
- **Adapter**: Alfa AWUS036ACS (USB, RTL8811AU chipset)
- **OS**: Kali Linux, Ubuntu 22.04 (ARM64 + x86_64 tested)
- **Drivers**: `rtl8812au` (Aircrack-ng maintained fork)
- **Wireless Tools**: 
  - `airmon-ng` – enable monitor mode
  - `airodump-ng` – passive packet capture
  - `aireplay-ng` – injection testing
- **Kernel Integration**: `DKMS` to support future kernel updates

---

####  **Methods / Architecture**
1. **Driver Installation**:
   - Cloned the Aircrack-ng maintained driver repository:
     ```bash
     git clone https://github.com/aircrack-ng/rtl8812au.git
     cd rtl8812au
     sudo make dkms_install
     ```
   - Verified module was loaded using `lsmod` and `iwconfig`.

2. **Testing Wireless Capabilities**:
   - Switched adapter to monitor mode using `airmon-ng`:
     ```bash
     airmon-ng start wlan0
     ```
   - Captured Wi-Fi traffic using `airodump-ng wlan0mon`.
   - Tested packet injection:
     ```bash
     aireplay-ng --test wlan0mon
     ```

3. **System Compatibility**:
   - Tested on both ARM (Raspberry Pi 5) and x86_64 (Mini PC) environments.
   - Used DKMS to ensure drivers persist across kernel upgrades.

---

####  **Skills Demonstrated**
- Installing and compiling kernel modules for external hardware
- Linux networking and wireless stack configuration
- Using Aircrack-ng suite for auditing and testing
- Managing driver persistence with DKMS
- Troubleshooting chipset-specific compatibility issues

---

####  **Screenshots**
![ACS 036](/assets/img/projects/wifi_adapters/ACS_036.jpg)
![Monitor Mode Enabled](/assets/img/projects/wifi_adapters/iwconfig_monitor_mode_blur.png)


---

####  **Links**
- [RTL8812AU Driver (Aircrack-ng)](https://github.com/aircrack-ng/rtl8812au)
- [Alfa AWUS036ACS Product Page](https://www.alfa.com.tw/products_show.php?pc=34&ps=216)

<br>
<br>