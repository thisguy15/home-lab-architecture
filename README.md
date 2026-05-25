# Architecture Overview  
This section documents the full architecture of the home‑lab environment, including compute nodes, networking, security systems, and distributed smart‑home components. Each diagram provides a focused view of a specific subsystem, and each subsystem is documented individually for clarity and maintainability.

---

# 📁 Diagrams Index

### **1. Full Home Infrastructure**  
A top‑level view of the entire digital estate, including servers, VLANs, IoT devices, and workshop nodes.  
➡️ [View Diagram](diagrams/home-infrastructure.md)

### **2. AI Compute Mesh**  
Shows how compute resources are distributed across the main server, dedicated AI server, and workshop AI server.  
➡️ [View Diagram](diagrams/ai-compute-mesh.md)

### **3. Security Mesh**  
Illustrates the ESP32‑S3 camera network, Raspberry Pi hub, and long‑term security backup server.  
➡️ [View Diagram](diagrams/security-mesh.md)

### **4. Network Layout**  
Displays VLAN segmentation and the ESP32‑S3 repeater mesh that strengthens wireless coverage.  
➡️ [View Diagram](diagrams/network-layout.md)

---

# 🧩 Subsystems (Active)

These are the systems that currently exist or are actively being built.

### **Mini Enterprise Cloud (5‑Node Architecture)**  
A distributed micro‑datacenter composed of:  
- OllamaPool (AI compute + model storage)  
- PlexPool (media)  
- DataBackupPool (family data + photos)  
- VMwarePool (virtual desktops + lab environments)  
- CommsPool (intercom, dashboards, automation)  

📄 `architecture/subsystems/mini-enterprise-cloud.md`

---

### **Portable Repair Kit (In Progress)**  
A sovereign, offline repair toolkit for helping people with IT issues without relying on USB drives, external HDDs, or cloud services.

📄 `architecture/subsystems/portable-repair-kit.md`

---

### **Homepage UI**  
Matrix‑style terminal dashboard for navigating the home‑lab.

📄 `architecture/homepage.md`

---

# 🧭 Roadmap & Future Planning

### **Roadmap (Future Subsystems + Major Projects)**  
All future subsystem ideas, hardware expansions, and long‑term projects are documented in:

📄 `architecture/roadmap.md`

Includes:  
- Portable Offline Repair Server (RPi Zero 2 W)  
- AI Helper Node (RPi 4)  
- Chromebook Thin‑Client Fleet  
- Mini Enterprise Cloud expansions  
- Future client‑layer integrations  

---

### **Future Improvements (Enhancements to Existing Systems)**  
Incremental upgrades, refinements, and optimizations are documented in:

📄 `future-improvements.md`

---

# 🧠 Architecture Decisions (ADRs)

Architecture decisions are documented in:

📄 `architecture/decisions/`

Current ADRs:  
- `nextcloud-to-immich.md`

---

# 🎯 Purpose of This Section

- Provide a clear visual understanding of the system  
- Document how each subsystem interacts  
- Support future upgrades and troubleshooting  
- Serve as a reference for new projects and expansions  
- Maintain a clean, modular, professional architecture index  

As the environment evolves, new diagrams and subsystems can be added to their respective folders and linked here.

---

# 🛠️ Future Diagram Additions (Optional)

- Smart Lighting System Diagram  
- Intercom System Diagram  
- Car Pi Nodes Diagram  
- Backup Server Architecture  
- Drive Rotation Workflow  
- Maker Projects (Tron Table, etc.)

---

# 📚 Repository Index (Top‑Level Docs)

For quick reference, the root of the repository includes:

- `README.md` — High‑level overview  
- `system-overview.md` — Broad architecture summary  
- `services.md` — Running services and roles  
- `network-layout.md` — Network reference  
- `troubleshooting.md` — Operational notes  

---

# Last Updated  
May 2026
