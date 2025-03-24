# 🏠 Home Wi-Fi Network Monitor Dashboard (Splunk)

This project analyzes and visualizes real-time traffic on a home Wi-Fi network using **Splunk** and **Wireshark**. I built this to simulate a SOC-style monitoring dashboard from scratch.

---

## 📌 What It Does

✅ Captures real network traffic  
✅ Tracks devices (by IP) connected to Wi-Fi  
✅ Shows what websites/devices they connected to  
✅ Identifies most/least active devices  
✅ Plots traffic trends over time

---

## 🔧 Tools Used

- 📡 **Wireshark** – captured `.pcap` data from home Wi-Fi
- 🔄 **CSV Export** – Wireshark logs saved as `.csv`
- 📊 **Splunk (Free Version)** – uploaded and visualized data using SPL
- 🧠 **SPL (Search Processing Language)** – used to build custom panels

---

## 📊 Dashboard Panels

| Panel Title               | Description                           |
|---------------------------|----------------------------------------|
| Most Active Devices       | Devices sending the most packets       |
| Least Active Devices      | Devices with minimal network activity  |
| Top Visited Sites         | Most contacted destination IPs         |
| Device ↔ Site Mapping     | Shows what each device accessed        |
| Traffic Trend             | Activity over time (timechart)         |

---

## 📸 Screenshots
[Dashboard Full View](Screenshot-1.png)  
[Panel View](Screenshot-3.png)

---


📌 [Connect with me on LinkedIn](https://www.linkedin.com/in/mvasamsetti/)
