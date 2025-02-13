---
title: Wi-Fi&#58; Everyone's Data, Everywhere, All the Time.
tags: [Wi-Fi Vulnerability, Hacking]
style: fill
color: light
description: Over 90% of US homes have a wireless access point, but how many people consider the related security issues.
---

Over 90% of US homes have a wireless access point, but how many people consider the related security issues. I would wager not many in the general public even know where to start other than creating a strong password. 

Generally speaking, the password is arguably the most important piece when it comes unauthorized access to your network. Yes, encryption protocols matter, WEP, WPA, WPA2, WPA3 in order of strength. The point I am making here is that even if your router has the strongest encryption and a 14 character password that looks like gibberish, yes brute forcing may be impossible, but if someone gets the password because you have it taped to the router, consider yourself hacked.

On the other hand, if you have a weak password (like 'pass12345') but strong encryption, someone may simply guess the password. However an even worse scenario, is having a weak password and weak encryption. This allows an attacker to capture data when a device, like your phone, connects to your home wifi. The captured data can then be run in a program to brute force guess the password compared to that captured data. It should be understood that gigantic wordlists exist of simple and common passwords, often exposed in data breaches.

Once someone has the correct password and connects to your network, they can passively sniff, capture packets, or scan the entire network for discovery, and assess your vulnerabilities. How many people would know that someone is on their network?, much less carrying out these activities.
 
Some routers are shipped with default passwords that are easily found on the internet. In fact, Wi-Fi signals carry MAC addresses that can be obtained without ever connecting to the access point if an attacker has an antenna capable of monitor mode. The MAC contains an OUI, which is the first 3 octets (XX:XX:XX), these values can be searched to reveal the vendor of the device. The default login for that vendor can be searched online to obtain a possible login method used by that vendor (like 'admin:admin', or common syntax of the login 'SpectrumWiFi-XXXX'). 

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