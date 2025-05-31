---
title: Web Development - Network Services Landing and Navigation Page
date: 2024-05-04 08:01:35 +0300
#subtitle: HTML, CSS, Docker, UI/UX 
image: '/images/dashboard_services.png'
#video_embed: https://www.youtube.com/embed/phiMxtqlFIY
github_url: https://github.com/blaine-geiger/home-network-dashboard
---

---

<a href="{{ page.github_url }}" target="_blank" style="text-decoration: none;">
  <img src="https://img.shields.io/badge/View%20The%20Details%20on-GitHub-181717?style=for-the-badge&logo=github" alt="View the full project on GitHub">
</a>

####  **Goals**
- Develop a centralized dashboard to ease navigation of network services web interfaces.

---

####  **Tools & Technologies**
- **Data Collection**: Telegraf
- **Time-Series Database**: InfluxDB
- **Visualization**: Grafana
- **Networking**: Home routers, switches, and connected devices
- **Deployment**: Docker Compose for container orchestration

---

####  **Methods / Architecture**
- **Telegraf**: Configured to collect metrics from various sources, including system stats and network data.
- **InfluxDB**: Set up as the time-series database to store collected metrics.
- **Grafana**: Connected to InfluxDB to create interactive dashboards displaying network performance, device uptime, and traffic analysis.
- **Docker Compose**: Utilized to deploy and manage Telegraf, InfluxDB, and Grafana containers efficiently.

---

####  **Skills Demonstrated**
- Setting up and configuring a full monitoring stack using Telegraf, InfluxDB, and Grafana.
- Creating custom dashboards to visualize complex network data.
- Implementing Docker Compose for streamlined deployment and management of services.
- Troubleshooting and optimizing data collection and visualization processes.

---

####  **Screenshots**
![Network Devices](/images/dashboard_devices.png)
![Network Services](/images/dashboard_services.png)

<br>
<br>