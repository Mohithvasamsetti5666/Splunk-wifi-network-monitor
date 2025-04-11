# 📡 Home Wi-Fi Network Monitor Dashboard (Splunk)

This project simulates a Security Operations Center (SOC)-style monitoring dashboard to analyze Wi-Fi traffic using Splunk.

---

## 🎯 Project Objective

Track and visualize:
- Devices connected to your Wi-Fi network
- Which websites/IPs they connect to
- Network traffic volume and trends

All done **offline**, using `.pcap` and `.csv` log files via Wireshark.

---

## 🛠️ Tools Used

| Tool       | Purpose                                 |
|------------|------------------------------------------|
| Wireshark  | Captured `.pcap` file from home network  |
| CSV Export | Converted `.pcap` to `.csv`              |
| Splunk     | Ingested `.csv` and built visual panels  |
| SPL        | Used to search, summarize, and visualize |

---

## 📁 Folder Contents

| File | Purpose |
|------|---------|
| `home_network_traffic.csv` | Raw Wi-Fi log data from Wireshark |
| `WIFITraffic_spl_queries.txt` | List of SPL queries used in Splunk panels |
| `Screenshot-1.png` | Dashboard full view |
| `Screenshot-2.png` | Most active devices |
| `Screenshot-3.png` | Device-to-site mapping |
| `Home Network Traffic Dashboard.pdf` | Optional PDF export |

---

## 📊 Dashboard Panels (Created in Splunk)

| Panel Title         | Description                                |
|---------------------|--------------------------------------------|
| Most Active Devices | Devices sending the most packets           |
| Least Active Devices| Devices with low packet count              |
| Top Visited Sites   | Most contacted IPs (websites, routers)     |
| Device ↔ Site Map   | Which device talked to which destination   |
| Traffic Trend       | Timeline of overall network usage          |

---

## 🔎 Example SPL Queries

**Most Active Devices**
```spl
| inputlookup home_network_traffic.csv
| stats count by "Source"
| sort - count
