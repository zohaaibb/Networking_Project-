# 🐍 Snort 3 Project

This folder contains files related to the setup and configuration of **Snort 3**, a high-performance Network Intrusion Detection and Prevention System (NIDS/NIPS).

## 📌 Overview

Unlike Snort 2, **Snort 3 does not come with pre-configured files or default rules**. Everything must be manually configured, which makes it more flexible but also more involved to set up.

This project demonstrates the process of:

- Installing and running Snort 3 from scratch
- Creating the **recommended directory structure**
- Writing and applying custom Snort rules
- Configuring the `snort.conf` file to include custom rule paths
- Generating alerts using test traffic

---

## 🗂️ Files in This Directory

- `snort.conf`: The main configuration file with paths, variables, and rule inclusions.
- `custom_rules.rules`: Contains user-defined Snort 3 rules for testing and detection.

---

All configurations were done manually for Snort 3.

Rules were tested on local network traffic.

Snort was run in packet sniffing and alerting mode.

The logs were reviewed to verify rule triggers.

👨‍💻 Author
Muhammad Zohaib Zafar


