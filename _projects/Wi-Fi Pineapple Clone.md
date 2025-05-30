---
title: Wi-Fi Pineapple Clone
date: 2024-11-01 08:01:35 +0300
#subtitle: PineAP, OpenWRT, Firmware Flashing
image: '/images/pineapple.jpg'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
---

<p align="center">
  <img src="/images/pineapple.gif" alt="My Image" width="400">
</p>

---

####  **Goals**
- Build a functional **Wi-Fi Pineapple clone** for wireless auditing and penetration testing.
- Utilize **low-cost, off-the-shelf hardware** to replicate the capabilities of commercial devices.
- Deploy **OpenWRT-based firmware** to enable features like rogue AP creation, client spoofing, and credential harvesting.

---

####  **Tools & Technologies**
- **Router**: GL.iNet GL-MT300N-V2 ("Mango") or GL-AR750S ("Slate")
- **Firmware**:
  - [OpenWRT 19.07.7](https://firmware-selector.openwrt.org/)
  - [Wi-Fi Pineapple Clone Firmware by xchwarze](https://gitlab.com/xchwarze/wifi-pineapple-cloner-builds)
- **Wi-Fi Adapter**: USB adapter with compatible chipset (e.g., RT5370 or MT7612U)
- **Software**: SSH client, SCP tool

---

####  **Methods / Architecture**

1. **Firmware Preparation**:
   - Download the appropriate OpenWRT 19.07.7 firmware for your router model.
   - Obtain the corresponding Wi-Fi Pineapple clone firmware from xchwarze's repository.

2. **Flashing OpenWRT**:
   - Access the router's firmware upgrade interface (typically at `192.168.8.1`).
   - Flash the OpenWRT firmware to the router.

3. **Installing Pineapple Clone Firmware**:
   - Use SCP or SFTP in CLI or an application like FileZilla to transfer the clone firmware to the router:
     ```bash
     scp clone-firmware.bin root@192.168.1.1:/tmp
     ```
   - SSH into the router and execute:
     ```bash
     sysupgrade -n -F /tmp/clone-firmware.bin
     ```
   - Wait for the router to reboot with the new firmware.

4. **Accessing the Pineapple Interface**:
   - Connect to the router's network.
   - Navigate to `http://172.16.42.1:1471` to access the Pineapple web interface.

5. **Module Installation**:
   - Plug in a USB drive to the router for additional storage.
   - Format the USB drive via the web interface.
   - Install desired modules for extended functionality.

---

####  **Skills Demonstrated**
- Firmware flashing and router configuration.
- Deployment of OpenWRT and custom firmware.

<!-- 
- Setup of rogue access points and wireless auditing tools.
- Integration of USB storage for module management. 
-->

---

####  **Screenshots**
![Wi-Fi Pineappe Clone](/images/pineapple.jpg)
<!--![Pineapple Web Interface](assets/img/pineapple-interface.png)
![Module Installation](assets/img/pineapple-modules.png)
![Rogue AP Setup](assets/img/pineapple-rogue-ap.png) -->

---

####  **Links**
- [xchwarze's Wi-Fi Pineapple Cloner GitHub Repository](https://github.com/xchwarze/wifi-pineapple-cloner)
- [OpenWRT Firmware Selector](https://firmware-selector.openwrt.org/)

<!--
- [YouTube Tutorial: Build a $23 Wi-Fi Pineapple in 6 Minutes](https://www.youtube.com/watch?v=udnxagkSzoA)
- [Pineapple Cloning Tutorial by CyberSpacemanMike](https://cyberspacemanmike.com/2024/09/20/pineapple-cloning-tutorial-pt-1-hardware-and-firmware/)
-->