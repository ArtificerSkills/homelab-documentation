# 🚫 Ad Blocker

## 📑 Table of Contents
- [Overview](#-overview)
- [Deployment](#-deployment)
- [Device Configuration](#-device-configuration)
- [Effectiveness](#-effectiveness)
- [Limitations](#-limitations)
- [Lessons Learned](#-lessons-learned)
- [Future Considerations](#-future-considerations)
- [Notes](#-notes)

---

## 📦 Overview

The home lab ad blocker was deployed as part of **TrueNAS Core**, providing network-wide ad blocking and improved browsing experience.

The goal was to **remove intrusive ads**, reduce background traffic, and create a cleaner web browsing environment across all devices.

---

## ⚙️ Deployment

- Platform: **TrueNAS Core**  
- Ad Blocker Service: **AdGuard (to be confirmed)**  
- Installation: Integrated plugin/jail-based deployment

**Notes:**  
- The ad blocker ran at the network level, intercepting traffic from all connected devices.  
- Required manual configuration for certain devices (PCs, TVs, mobile devices) to ensure traffic routed through the ad blocker.

---

## 🖥️ Device Configuration

- Devices required manual IP assignment or DNS settings to route through the ad blocker.  
- Devices affected included:
  - PCs  
  - Smart TVs  
  - Mobile phones  
- Configuration specifics will be documented once the TrueNAS system is accessible.

---

## 📊 Effectiveness

The ad blocker provided significant improvements:

- Reduced **background ad traffic** on websites  
- Enabled **cleaner, less cluttered browsing**  
- Worked reliably across multiple devices

**Exceptions / Notes:**  
- Certain websites, e.g., Wowhead or Raider.io, detected ad blocking and requested users to disable it.  
- Despite these edge cases, overall performance and effectiveness were very good.

---

## ⚠️ Limitations

- Manual device configuration was required to ensure traffic passed through the ad blocker.  
- Exact traffic metrics and performance statistics are not yet recorded.  
- Integrated TrueNAS Core solution may not be fully flexible for future networks.

---

## 📝 Lessons Learned

- Network-wide ad blocking works well but requires careful device setup.  
- Maintaining documentation for configuration is essential for future redeployment.  
- AI-assisted troubleshooting helped navigate unclear instructions during setup.

---

## 🚀 Future Considerations

- Verify exact ad blocker service used (likely AdGuard) and document version.  
- Extract configuration files from TrueNAS for **future redeployment**.  
- Consider exploring alternative ad blocking solutions for improved flexibility and ease of management.  
- Automate device routing to minimize manual configuration in future setups.

---

## 📝 Notes

- Configuration screenshots, logs, and IP setup details will be added once the TrueNAS system is accessible.  
- This README serves as a **living document** to guide future deployments and network setups.
