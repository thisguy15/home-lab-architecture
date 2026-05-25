# Project Priority Roadmap  
*A balanced, momentum‑driven build sequence for the sovereign home‑lab ecosystem.*

This roadmap outlines the phased development of the home infrastructure, compute mesh, security systems, and smart‑home components. It is designed for steady progress without burnout, respecting real‑life schedules and energy cycles.

---

# Phase 1 — Core Stability & Foundation  
**High impact, low friction — unlocks everything else.**

- Finalize repo structure and architecture documentation  
- Validate TrueNAS configuration (pools, datasets, permissions, snapshots)  
- Bring Backup Server online in basic mode  
- Ensure core services (Plex, Immich, Syncthing) are stable  

**Outcome:**  
A clean, documented, stable foundation for all future phases.

---

# Phase 2 — Storage & Backup Architecture  
**Your data becomes resilient before anything else grows.**

- Configure ZFS replication (TrueNAS → Backup Server)  
- Establish snapshot schedules (daily + weekly)  
- Create encrypted backup datasets  
- Document drive rotation workflow  
- Validate Syncthing and Immich reliability  

**Outcome:**  
Redundant, sovereign, long‑term data protection.

---

# Phase 3 — Network & Coverage Expansion  
**The system breathes. Everything gets stronger.**

- Finalize VLAN segmentation (Main LAN, IoT, Workshop)  
- Apply firewall rules and isolation policies  
- Deploy ESP32‑S3 repeater mesh for whole‑home coverage  
- Strengthen workshop connectivity (WiFi + Tailscale)  

**Outcome:**  
A robust, segmented, high‑coverage network ready for distributed systems.

---

# Phase 4 — AI Compute Mesh Buildout  
**Your distributed compute triangle comes alive.**

- Configure Dedicated AI Server (GPU, drivers, containers)  
- Bring Workshop AI Server online for edge inference  
- Establish model sync strategy (Syncthing, ZFS send, or manual)  
- Validate cross‑node communication over Tailscale  

**Outcome:**  
A flexible, resilient, multi‑node AI compute mesh.

---

# Phase 5 — Security Mesh Deployment  
**A fully local, privacy‑first security system.**

- Flash and configure ESP32‑S3 cameras  
- Deploy Raspberry Pi Security Hub (event ingestion + local AI)  
- Integrate Backup Server for long‑term retention  
- Validate motion → detection → storage pipeline  

**Outcome:**  
A sovereign, cloud‑free security system with redundancy.

---

# Phase 6 — Smart Home Systems  
**Comfort, convenience, and control — all local.**

- Deploy ESP32‑S3 smart lighting nodes  
- Install and configure ESP32‑S3 intercom system  
- Build automation logic (time, presence, event‑based)  
- Integrate with compute mesh where needed  

**Outcome:**  
A responsive, intentional smart‑home environment.

---

# Phase 7 — Maker & Creative Projects  
**The fun stuff — once the infrastructure is rock solid.**

- Car Pi nodes (music server, FM/Bluetooth, supercap UPS)  
- Retro gaming station  
- Tron table and LED projects  
- Workshop automation enhancements  

**Outcome:**  
Creative, playful, high‑impact projects built on a stable foundation.

---

# Future Subsystems & Projects  
*Long‑term expansions that extend the home‑lab ecosystem beyond core infrastructure.*

---

## 🔧 Portable Offline Repair Server (RPi Zero 2 W — Altoids Tin Build)  
A pocket‑sized, battery‑powered offline repair server housed in an Altoids tin.  
Designed as a sovereign, portable field‑tech kit for repairing Windows, macOS, and Linux systems.

**Planned Features:**  
- Lithium battery for fully portable operation  
- Runs as a WiFi AP or joins existing networks  
- Multi–microSD storage array (RAID‑style) for tool hosting  
- Hosts repair tools, ISOs, drivers, malware utilities, diagnostics, and portable apps  

**Why:**  
USB drives fail, external HDDs disconnect, CD drives are gone, and IoT file servers are unreliable.  
This provides a simple, offline, always‑available toolkit for helping people with IT issues.

---

## 🧠 AI Helper Node (RPi 4)  
A secondary node that connects to the RPi Zero via WiFi to provide:

- Offline AI troubleshooting  
- Log analysis  
- Tool recommendations  
- Step‑by‑step repair guidance  
- Local LLM‑based support  

Together, the RPi Zero and RPi 4 form a portable, AI‑augmented repair station.

---

## 💻 Chromebook Thin‑Client Fleet (3–5 Devices)  
A future client layer for the home mini‑enterprise cloud.

**Planned Capabilities:**  
- Thin‑client access to VMware desktops  
- Tailscale‑secured access to all internal pools  
- Lightweight admin consoles for field‑tech work  
- Simple scripts for printing on other people’s WiFi  
- Portable, low‑maintenance endpoints for family and support scenarios  

**Why:**  
To create a simple, reliable, portable client layer for accessing the home cloud and helping people with IT issues without relying on USB drives or unstable storage devices.

---

## ☁️ Mini Enterprise Cloud Expansion (5‑Node Architecture)  
Future enhancements to the distributed cloud system:

- OllamaPool (AI compute + model storage)  
- PlexPool (media)  
- DataBackupPool (family data + photos)  
- VMwarePool (virtual desktops + lab environments)  
- CommsPool (intercom, dashboards, automation)  

**Future Additions:**  
- DAC storage expansion upgrades  
- Additional compute nodes  
- More Tailscale‑connected clients  
- Integration with Chromebook fleet  

---

# How to Use This Roadmap

- Work in **energy windows**, not deadlines  
- Each phase is **modular** — pause anytime  
- Every step builds on the last  
- Update this file as the system evolves  

---

# Last Updated  
May 2026
