---
title: Linux Server, Logging, and Visualization
date: 2024-12-01 08:01:35 +0300
#subtitle: Ubuntu, Docker, Prometheus, Grafana
image: '/images/server.jpg'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
---

<!--
<a href="{{ page.github_url }}" target="_blank" style="text-decoration: none;">
  <img src="https://img.shields.io/badge/View%20The%20Details%20on-GitHub-181717?style=for-the-badge&logo=github" alt="View the full project on GitHub">
</a>
-->

---
<p align="center">
  <img src="/images/server.gif" alt="My Image" width="500">
  <p align="center">
    YouTube - Craft Computing
  </p>  
</p>

---
####  **Goals**
Establish a centralized observability stack in a home lab environment:
- Collect firewall logs from pfSense
- Scrape server metrics from a Raspberry Pi 5 based Ubuntu 
- Aggregate and visualize Fail2Ban logs
- Build dashboards for real-time monitoring, alerts, and behavioral insights

---

####  **Tools & Technologies**
- **Hardware**: pfSense SG-1100, Raspberry Pi 5 (Ubuntu Server ARM64)
- **Containerized Stack**: Docker + Docker Compose
- **Monitoring**: Telegraf, InfluxDB, Grafana
- **Log Forwarding**: Promtail for pfSense syslog, systemd journal scraping
- **Security**: Fail2Ban with real-time Grafana dashboard integration
- **Visualization**: Custom dashboards in Grafana (network, CPU/RAM, bans, firewall events)

---

#### **Methods / Architecture**
- Configured **Telegraf** to scrape host metrics and send them to **InfluxDB**
- Parsed **pfSense** logs via **Promtail**, forwarding to Loki for visualization
- Integrated **Fail2Ban** logs using Telegraf's `exec` and `tail` plugins
- Built custom Grafana dashboards:
  - Live firewall traffic analysis
  - Fail2Ban: bans over time, IP origin, frequency, jail-specific stats
  - System resource usage and container health
- All services deployed and managed via **Docker Compose**

---

####  **Skills Demonstrated**
- Self-hosted logging and monitoring stack deployment
- Query construction for Grafana visualizations (InfluxQL / LogQL)
- Secure syslog forwarding across physical and virtual subnets
- Dashboard development and log correlation
- Fail2Ban hardening + visualization for brute-force detection
<br>
<br>