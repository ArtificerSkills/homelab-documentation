# 🎬 Plex Media Server

## 📑 Table of Contents
- [Overview](#-overview)
- [Deployment Method](#-deployment-method)
- [Storage Configuration](#-storage-configuration)
- [Media Library](#-media-library)
- [Access & Usage](#-access--usage)
- [Discord Integration](#-discord-integration)
- [Challenges & Troubleshooting Experience](#-challenges--troubleshooting-experience)
- [Monetisation (Cost Recovery)](#-monetisation-cost-recovery)
- [Limitations & Lessons Learned](#-limitations--lessons-learned)
- [Future Improvements](#-future-improvements)
- [Notes](#-notes)

---

## 📦 Overview
Plex was deployed as part of the NAS system to provide a **centralised media server** for both personal use and community access.

It was used for:
- Local media streaming (TV)
- Remote access for selected users
- Integration with Discord for shared viewing experiences

---

## ⚙️ Deployment Method

- Platform: **TrueNAS Core**
- Installation Type: **Plex Plugin (Jail-based)**

### Configuration
- Plex was deployed inside a **TrueNAS jail**
- Storage was mounted into the jail via **pools**

> ⚠️ Exact configuration steps and mount points will be documented later

---

## 💾 Storage Configuration

### Setup
- Storage type: **ZFS Pool (non-redundant)**
- Drives:
  - Approx. **3x high-capacity HDDs**
  - Estimated: ~4TB each *(to be confirmed)*

### Important Note
- ❌ **No redundancy configured**
- ❌ No RAID setup (e.g., RAIDZ, RAID1)

### Result
- Drives were effectively combined into a **single large storage pool**
- **Any drive failure would result in total data loss**

> ⚠️ This was a conscious trade-off due to limited hardware and cost constraints at the time

---

## 🎞️ Media Library

- Library size: **400+ movies**
- Content stored locally on NAS drives

### Performance
- Worked reliably for:
  - Local playback
  - Direct streaming to TV

---

## 📺 Access & Usage

### Local Access
- Plex app installed directly on TV
- Allowed seamless in-home streaming

### Remote Access
- Enabled for selected users
- Provided access via personal Plex accounts

---

## 🤖 Discord Integration

One of the most unique features of this setup was **Discord-based media control**, powered by an external bot.

### GitHub Repository
- [Plex Discord Bot by danxfisher](https://github.com/danxfisher/Plex-Discord-Bot)

---

### How It Worked
1. User joins a **Discord voice channel**
2. Uses a **slash command** in a text channel
3. Bot retrieves:
   - Plex media library
4. User selects a movie
5. Playback is triggered on a **dedicated streaming PC**

---

### Components Involved
- Plex Media Server (NAS)
- Discord Bot (external GitHub project)
- Separate **Streaming PC**

---

### Playback Method
- Streaming PC used a Plex client (HTPC-style interface)
- Media was then streamed into Discord for shared viewing

---

### Notes
- Bot configuration and customisation will be documented in `/plex/scripts/` in the future
- Additional setup steps (API keys, authentication, etc.) to be added later

---

## 🧠 Challenges & Troubleshooting Experience

### 📚 Learning Curve
This implementation involved a steep learning curve, particularly around:

- Importing and working with external GitHub repositories
- Deploying third-party tools within TrueNAS Core
- Understanding how services interact across systems (NAS, Discord, streaming PC)

At the time, this was a completely new area, and troubleshooting required extensive research and experimentation.

---

### 🧩 Repository Issues
The Discord bot implementation was based on an older repository:

- Estimated age: ~9 years
- Some functionality was **outdated or partially broken**

Changes to:
- Plex APIs  
- Dependency versions  
- System architecture  

…meant that parts of the code required troubleshooting and workarounds to function correctly.

---

### ⚙️ Platform Constraints
Using **TrueNAS Core** introduced additional challenges:

- Jail-based system is less flexible than modern container platforms
- Harder to manage dependencies compared to Docker-based environments
- Increased complexity when integrating external tools

---

### 🤖 Troubleshooting Approach
Troubleshooting relied heavily on:

- Documentation
- Trial and error
- AI-assisted debugging

Despite these challenges, the system was successfully made to function for its intended use.

---

### 💾 Configuration Status
- All configurations currently exist on the original NAS system
- The system is in storage and not currently accessible

---

### 🔄 Future Plan
- Extract configs and scripts from the NAS
- Store them in this repository under:
  - `/plex/configs/`
  - `/plex/scripts/`

This will allow:
- Easier redeployment
- Version control
- Long-term maintainability

---

## 💰 Monetisation (Cost Recovery)

Plex access was also used as a **community perk**.

### Context
- Offered to members supporting the guild via Patreon

### Purpose
- ❌ Not for profit
- ✅ Help offset:
  - Power usage
  - Hardware wear
  - Server uptime costs

### Outcome
- Provided value to users
- Encouraged engagement within the community

---

## ⚠️ Limitations & Lessons Learned

### Storage Design
- Lack of redundancy was the biggest risk
- No fault tolerance → total data loss scenario

👉 This highlights the importance of:
- RAID / redundancy
- Backup strategies

---

### Platform Choice
- TrueNAS Core:
  - Jail system felt restrictive over time
  - Less flexible than modern container solutions

---

### Hardware Constraints
- NAS hardware was not powerful enough for:
  - Real-time transcoding
  - Streaming to Discord

---

## 🚀 Future Improvements

### Storage
- Implement proper redundancy:
  - RAIDZ1 / RAIDZ2
  - Or mirrored drives

### Platform
- Migrate to **TrueNAS Scale**
  - Docker-based workloads
  - Easier service management

### Architecture
- Reduce reliance on:
  - Separate streaming PC
- Move toward:
  - Direct streaming solutions
  - GPU-assisted transcoding

---

## 📝 Notes
- Drive models, capacities, and exact pool configuration will be updated later
- Discord bot repository and configuration will be added
- Scripts and configs will be documented in their respective folders:
  - `/plex/configs/`
  - `/plex/scripts/`
