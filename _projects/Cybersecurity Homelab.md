---
title: Cybersecurity Homelab
date: 2024-11-05 08:01:35 +0300
#subtitle: Networking, Administration, Virtualization
image: '/images/homelab.jpg'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
github_url: https://github.com/blaine-geiger/homelab
---

<div style="text-align: center; margin: 1rem 0;">
  <img src="/images/network.gif" alt="My Image" width="500" style="display: block; margin: 0 auto;">
</div>

---

<a href="{{ page.github_url }}" target="_blank" style="text-decoration: none;">
  <img src="https://img.shields.io/badge/View%20The%20Details%20on-GitHub-181717?style=for-the-badge&logo=github" alt="View the full project on GitHub">
</a>

This project reflects some of my first steps into establishing a home lab environment. It involves the design, planning, and development of a home lab, segmented from my everyday home network, using both physical hardware and virtualization. This required fundamental knowledge of networking, hardware and software configurations, firewall and system administration, and virtualization.

After successfully installing the necessary components, I used VMware Workstation to recreate a large portion of the virtual environment and machines that existed in my University's cybersecurity lab, some of these include Kali Linux, Metasploitable2, OWASP, WebGoat, and DVWA.

The diagram below shows the layout of the network, subnets, and devices.

![Homelab Screenshot](/images/network_final.png)


Troubleshooting and self-guided learning were a large part of this project's successful outcome, and I developed valuable skills in:
* Deployment and Configuration
* Network Segmentation
* Firewall Rules
* IP Addressing
* Subnetting
* VLANs
* DHCP
* DNS

Cost considerations were weighed with performance, flexibility, scalability, power consumption, and physical space. Hardware  I decided on a small form factor PC , a managed switch, and a firewall appliance. The PC is flexible and scalable with 2 NICs, 2 nVME slots, and upgradeable RAM (64GB total max (32G x 2)). I will take full advantage of these specifications in later projects.

#### **Basic Steps**
1. Diagram basic network compnents while considering IP addressing scheme, including gateways, DNS, and DHCP servers and pools.
2. Firewall Configuration
    - Change router default IP, disable router's DHCP server, change router to AP mode.
    - Set firewall DNS server, configure firewall interfaces (WAN, LAN, OPT), including needed DNS and DHCP servers and pools.
    - Configure necessary baseline firewall rules for each interface.
3. Managed Switch
    - Disable DHCP on switch
    - Set static IP address for switch


<p><a href="https://github.com/blaine-geiger/homelab" target="_blank" style="text-decoration: none;">
  <img src="https://img.shields.io/badge/View%20The%20Details%20on-GitHub-181717?style=for-the-badge&logo=github" alt="View the full project on GitHub">
</a>

<br>
<br>
