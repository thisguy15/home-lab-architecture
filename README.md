Architecture Overview  
This section documents the full architecture of the home‑lab environment, including compute nodes, networking, security systems, and distributed smart‑home components. Each diagram provides a focused view of a specific subsystem, and each subsystem is documented individually for clarity and maintainability.  
  
📁 Diagrams Index  
1. Full Home Infrastructure  
A top‑level view of the entire digital estate, including servers, VLANs, IoT devices, and workshop nodes.  
➡️ View Diagram  
  
2. AI Compute Mesh  
Shows how compute resources are distributed across the main server, dedicated AI server, and workshop AI server.  
➡️ View Diagram  
  
3. Security Mesh  
Illustrates the ESP32‑S3 camera network, Raspberry Pi hub, and long‑term security backup server.  
➡️ View Diagram  
  
4. Network Layout  
Displays VLAN segmentation and the ESP32‑S3 repeater mesh that strengthens wireless coverage.  
➡️ View Diagram  
  
🧩 Subsystems (Active)  
These are the systems that currently exist or are actively being built.  
  
Mini Enterprise Cloud (Single-Node TrueNAS Core)  
A distributed storage and compute micro-datacenter composed of:  
* **OllamaPool:** AI compute, local LLM storage, and primary Docker stacks.  
* **PlexPool:** Media library hosting and Tautulli analytics.  
* **DataBackupPool:** Encrypted family backups (Immich/Syncthing).  
📄 architecture/subsystems/mini-enterprise-cloud.md  
  
Breuer Media Vault (BMV) — *Stable*  
A custom, self-cleaning, dark-mode responsive video downloader run in Docker (`yt-easy-downloader`). Features auto-cleanup script, PWA manifest for mobile bypass, and integrated dual-channel IT helpdesk hooks.  
📄 architecture/subsystems/breuer-media-vault.md  
  
Project FrankenTok — *In Progress (Architecture Complete)*  
A sovereign, zero-login family vertical video platform (TikTok clone). Features a strict 500GB dataset limit, dual-pass automated ingestion (`yt-dlp`), a JavaScript/Swiper.js watch-tracker, a Darwinian SQLite cleanup daemon (The Grim Reaper), and an AI Matchmaker linking Open WebUI to Gemini Flash.  
📄 architecture/subsystems/frankentok.md  
  
Home Assistant Integration — *In Progress*  
Migrating local smart home automation, Zigbee/Z-Wave coordinators, and integrating Open WebUI directly into the Home Assistant dashboard UI.  
📄 architecture/subsystems/home-assistant.md  
  
Portable Repair Kit — *In Progress*  
A sovereign, offline repair toolkit for helping people with IT issues without relying on USB drives, external HDDs, or cloud services.  
📄 architecture/subsystems/portable-repair-kit.md  
  
Homepage UI  
Matrix‑style terminal dashboard for navigating the home‑lab.  
📄 architecture/homepage.md  
  
🧭 Roadmap & Future Planning  
Roadmap (Future Subsystems + Major Projects)  
All future subsystem ideas, hardware expansions, and long‑term projects are documented in:  
  
📄 architecture/roadmap.md  
  
Includes:  
* Portable Offline Repair Server (RPi Zero 2 W)  
* AI Helper Node (RPi 4)  
* Chromebook Thin‑Client Fleet  
* Future client‑layer integrations  
  
Future Improvements (Enhancements to Existing Systems)  
Incremental upgrades, refinements, and optimizations are documented in:  
  
📄 future-improvements.md  
  
🧠 Architecture Decisions (ADRs)  
Architecture decisions are documented in:  
  
📄 architecture/decisions/  
  
Current ADRs:  
* `nextcloud-to-immich.md`  
* `frankentok-darwinian-cleanup.md` *(The retention rules for watched vs. skipped videos)*  
  
🎯 Purpose of This Section  
* Provide a clear visual understanding of the system  
* Document how each subsystem interacts  
* Support future upgrades and troubleshooting  
* Serve as a reference for new projects and expansions  
* Maintain a clean, modular, professional architecture index  
  
As the environment evolves, new diagrams and subsystems can be added to their respective folders and linked here.  
  
🛠️ Future Diagram Additions (Optional)  
* Smart Lighting System Diagram  
* Intercom System Diagram  
* Car Pi Nodes Diagram  
* Backup Server Architecture  
* Drive Rotation Workflow  
* Maker Projects (Tron Table, etc.)  
  
📚 Repository Index (Top‑Level Docs)  
For quick reference, the root of the repository includes:  
* README.md — High‑level overview  
* system-overview.md — Broad architecture summary  
* services.md — Running services and roles  
* network-layout.md — Network reference  
* troubleshooting.md — Operational notes  
  
Last Updated  
October 2026  