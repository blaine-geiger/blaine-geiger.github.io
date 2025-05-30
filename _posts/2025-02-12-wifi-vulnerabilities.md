---
layout: post
title: Wi-Fi (Everyone's Data, Everywhere, All the Time)
date: 2024-04-05 15:01:35 +0300
image: '/images/wifi.jpg'
---

Over 90% of US homes have a wireless access point, but how many people consider the related security issues. I would wager not many in the general public even know where to start other than creating a strong password. 

<i>Generally speaking</i>, the password is one of the main aspects a basic non-technical user will control when it comes to their home Wi-Fi security.
Yes, encryption protocols matter, WEP, WPA, WPA2, WPA3 in order of strength.

The point I am making here is that even if your router has the strongest encryption and a 14 character password that looks like gibberish, yes brute forcing may be impossible, but if someone gets the password because you have it taped to the router, consider yourself hacked.

On the other hand, if you have a weak password (like 'pass12345') but strong encryption llke WPA3. Someone may simply guess the password. However an even worse scenario, is having a weak password AND weak encryption. This allows an attacker to capture handshake data when a device, like your phone, connects to your home wi-fi. 

The handshake data contains cryptographic hash data that can then used by tools such as `hashcat`, to leverage dictionary attacks or brute-force attacks that can posssibly recover the password. This is all <b>without ever being to connected to the network!</b>. It should be understood that gigantic wordlists exist of simple and common passwords, often exposed in data breaches.

Once someone has the correct password and <i>does</i> connect to your network, they can capture packets, or scan the entire network for discovery, assess your vulnerabilities, and take time to plan an atack. How many average users would know that someone is on their network? Or carrying out these activities?
 
Many routers are shipped with default passwords that are easily found on the internet. In fact, Wi-Fi signals carry MAC addresses that can be obtained without ever connecting to the access point if an attacker has an antenna capable of monitor mode.

The MAC contains an OUI, which is the first 3 octets (XX:XX:XX), these values can be searched to reveal the vendor of the device. The default login for that vendor can be searched online to obtain a possible login method used by that vendor (like 'admin:admin', or common syntax of the login 'SpectrumWiFi-XXXX'). 

Other Wi-Fi related attacks exist as well, such as:
- ARP Spoofing/MITM
- DNS Spoofing
- Rogue Access Points/Evil Twin
- WPS Attacks

These attacks move beyond the scope of this write up, and I am not writing an entire textbook chapter here. What I want the reader to understand is that the modern prevalance of Wi-Fi coupled with most people's lack of understanding of the technology or proper security measures, can be a recipe for trouble. Let me offer some basic suggestions to harden your home Wi-Fi.

**How To Secure Your Wi-Fi**
- Use WPA3 encryption if your AP allows.
- Set up a strong password (16 characters, alphanumeric, special characters, unordered).
- Change the default router administration credentials.
- Use a guest network to keep connection visitors isolated.
- Disable WPS, you probably will not use it anyway.
- Learn how to update the AP's firmware to patch security issues. It is done via the admin console of the device.

— Blaine Geiger, 2-12-2025