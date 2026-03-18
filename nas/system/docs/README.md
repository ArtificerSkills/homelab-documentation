# 🖥️ NAS System

## 📑 Table of Contents
- [Overview](#-overview)
- [Hardware](#-hardware)
- [Operating System](#-operating-system)
- [Core Services](#-core-services)
- [Custom Use Cases](#-custom-use-cases)
- [Streaming Setup](#-streaming-setup)
- [Limitations & Lessons Learned](#-limitations--lessons-learned)
- [Future Improvements](#-future-improvements)
- [Notes](#-notes)

---

## 📦 Overview
The NAS (Network Attached Storage) was built using an **old desktop PC**, repurposed to act as a centralised home lab server.

This system served as:
- Media server
- Ad blocker
- Experimentation platform
- Hosting environment for custom bots

> ⚠️ This system is currently in storage and will be revisited for full hardware validation.

---

## 🧰 Hardware

### Base System
- Type: **Repurposed Desktop PC**
- RAM: **DDR3 (estimated)**
- CPU: **Legacy AMD processor (unconfirmed)**
- Core Count: **Possibly single-core**

> ⚠️ Hardware specifications are based on memory and will be confirmed later.

### Modifications
Additional hardware was added to support NAS functionality:
- Storage drives (configuration to be documented)
- Possible upgrades to improve usability

---

## 💽 Operating System

### Initial Deployment
- **FreeNAS**

### Final Deployment
- **TrueNAS Core**

### Notes
- Migration performed from FreeNAS → TrueNAS Core
- System remained on **Core**, not upgraded to Scale

---

## ⚙️ Core Services

The NAS hosted several core services:

### 🛡️ Ad Blocker
- Deployed using TrueNAS built-in capabilities
- Likely configured via plugin or jail

### 🎬 Plex Media Server
- Installed and managed within TrueNAS
- Used for local media streaming

> ⚠️ Exact deployment method (jail/container/plugin) to be confirmed

---

## 🧪 Custom Use Cases

The NAS was also used for experimentation, including:

- Hosting **custom Discord bots**
- Integrating services across the home lab
- Testing self-hosted environments

One notable implementation:
- A Discord bot that allowed users to **trigger Plex media playback**

---

## 📺 Streaming Setup

To enable Discord-based streaming:

### Additional Component
- Separate **Streaming PC**

### Function
- Acted as an intermediary between:
  - Plex Media Server
  - Discord voice/video channels

### Reason
The NAS itself was not powerful enough to:
- Handle real-time streaming
- Encode/transcode media for Discord

---

## ⚠️ Limitations & Lessons Learned

### Performance Constraints
- Legacy hardware limited:
  - Processing power
  - Expandability
  - Service scalability

### Platform Choice
- **TrueNAS Core limitations:**
  - Less flexible for modern container workloads
  - Plugin/jail system less intuitive than containers

---

## 🚀 Future Improvements

### Planned Changes
- Move to **TrueNAS Scale**
  - Better support for containers (Docker/Kubernetes)
  - Greater flexibility for modern workloads

### Hardware Upgrade
- Replace legacy system with:
  - Multi-core CPU
  - Higher RAM capacity
  - Improved storage configuration

---

## 📝 Notes
- Full hardware specifications will be updated once retrieved from storage
- Service configurations (Plex, Ad Blocker) will be documented in their respective folders:
  - `/nas/plex/`
  - `/nas/ad-blocker/`
  - `/nas/system/`

---
