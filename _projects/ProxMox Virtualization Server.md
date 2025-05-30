---
title: ProxMox Virtualization Server
date: 2025-03-15 08:01:35 +0300
#subtitle: 
image: '/images/proxmox_dashboard.png'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
---

<!-- > View the [Github Repository](https://www.github.com/blaine-geiger/Proxmox-Server) -->

####  **Goals**
- Deploy **Proxmox VE** as the core hypervisor to upscale cybersecurity lab environment.
- Configure a **local Certificate Authority (CA)** and issue a custom TLS certificate for the Proxmox Web UI.
- Harden the host with secure access, disk management, and system tuning for long-term virtual machine hosting.

---

####  **Tools & Technologies**
- **Hypervisor**: Proxmox VE 8.x (bare-metal installation)
- **OS Filesystem**: ZFS (for storage redundancy and snapshotting)
- **TLS/SSL**: OpenSSL, Local Certificate Authority
- **Access Methods**: SSH, Web UI (HTTPS)
- **Hardware**: x86_64 Mini PC with 2 NICs, 2 SSD/NVMe storage slots, expanded to 64 GB RAM

---

####  **Methods / Architecture**

1. **Proxmox Installation**:
   - Flashed ISO to USB and installed on bare metal.
   - Configured static IP, hostname, and ZFS as the root filesystem for snapshot capabilities.

2. **Web UI Hardening**:
   - Disabled the self-signed default certificate warnings by generating a custom certificate signed by a local CA.
   - Generated a **Certificate Signing Request (CSR)** on the Proxmox host.
   - Imported the CSR into the **internal Certificate Authority (CA)** on the **pfSense firewall**.
   - Signed the certificate through the pfSense CA and downloaded:
     - The signed certificate
     - The root CA certificate
   - Uploaded both the signed certificate and the private key to Proxmox
   - Imported the firewall's root CA into browser and system trust stores on admin devices to prevent browser warnings.

3. **Initial Proxmox Configuration**:
   - Created separate storage pools for ISOs, backups, and VM disks.
   - Enabled **NTP**, system logs, and updated the APT repo sources.
   - Added **no-subscription** Proxmox repo for package updates.

4. **SSH and Admin Access**:
   - Hardened SSH access:
     - Disabled root login with password.
     - Created a non-root admin account with `sudo` privileges.
   - Setup public key authentication for remote management.

5. **Backup & Networking Prep**:
   - Created a backup routine (manual or scheduled via `vzdump`) to external USB or network location.
   - Reserved and labeled additional NICs for use with future VLAN segmentation and pfSense virtualized interfaces.

---

####  **Skills Demonstrated**
- Bare-metal deployment and configuration of enterprise-grade hypervisors.
- OpenSSL: Generating and managing a local CA and certificates.
- Linux CLI system administration, Proxmox tuning, and repo management.
- Secure networking and remote management best practices.
- Filesystem planning for container and VM performance (ZFS, LVM).

---

####  **Screenshots**
![Proxmox Dashboard](/images/proxmox_dashboard.png)

---

####  **Links**
- [Proxmox VE Documentation](https://pve.proxmox.com/wiki/Main_Page)
- [Proxmox No-Subscription Repo Setup](https://pve.proxmox.com/wiki/Package_Repositories)

<br>
<br>