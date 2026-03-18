# 🌐 Network Cabling Overview

## 📑 Table of Contents
- [Cabling Choice](#-cabling-choice)
- [Context at Time of Installation](#-context-at-time-of-installation)
- [Current Limitations](#-current-limitations)
- [Reflection](#-reflection)
- [Future Considerations](#-future-considerations)
- [Notes](#-notes)

---

## 🧵 Cabling Choice

The network infrastructure for this project was installed using **CAT5e (Category 5e)** cabling throughout the property.

At the time of installation (circa 2020–2021), this decision was based primarily on **cost-efficiency** and the **available internet speeds**. CAT5e was significantly cheaper than CAT6 and CAT6A, while still exceeding the requirements of the connection available at the time.

**Notes:**  
- Chosen to balance performance and cost  
- Exceeded ISP requirements at the time  

---

## 📊 Context at Time of Installation

- Maximum available internet speed: ~500 Mbps (0.5 Gbps)  
- CAT5e rated performance: up to 1 Gbps over typical residential distances

Given these constraints, CAT5e provided:  
- ✅ Sufficient bandwidth headroom  
- ✅ Reliable performance  
- ✅ Lower overall installation cost

This made it a practical and justified decision at the time.

---

## ⚠️ Current Limitations

Since installation, available internet speeds in the area have increased significantly:  

- 1 Gbps connections are now common  
- 2 Gbps fibre connections are becoming available

While CAT5e can technically support up to 1 Gbps, it becomes a limiting factor in scenarios involving:  
- Multi-gigabit internet connections  
- High-throughput internal network traffic  
- Future scalability

As a result, the existing cabling infrastructure is now a **performance bottleneck**.

---

## 📝 Reflection

In hindsight, installing **CAT6A** cabling would have been a more future-proof solution, offering:  

- ⚡ Support for 10 Gbps speeds  
- 🛡️ Better shielding and reduced interference  
- 📈 Longer-term scalability

However, this must be viewed in the context of:  
- 💰 Budget constraints at the time  
- 🌐 Available ISP speeds  
- 🛠️ Practical decision-making based on known requirements

---

## 🚀 Future Considerations

To remove current limitations and support higher speeds, a full re-cabling to **CAT6 or CAT6A** would be required.

This would:  
- ✅ Eliminate the current bottleneck  
- ✅ Enable multi-gig networking  
- ✅ Align the infrastructure with modern and future network demands

---

## 📝 Notes

- All cabling choices should be reviewed in the context of **future ISP upgrades**.  
- Any new device deployments requiring multi-gigabit speeds may require a **cabling upgrade**.  
- Visual diagrams of the cabling layout can be added to `/network/images/` in future iterations.
