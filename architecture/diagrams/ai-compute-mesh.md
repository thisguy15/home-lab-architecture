# AI Compute Mesh Architecture

This diagram illustrates the distributed AI compute mesh across the home-lab. It shows how the main TrueNAS server, the dedicated AI server, and the workshop AI server work together to provide scalable, resilient, and location-aware compute resources.

---

## Diagram: AI Compute Mesh

```
                 ┌───────────────────────────────┐
                 │      Main TrueNAS Server      │
                 │  - Storage pools              │
                 │  - Plex / Immich / Syncthing  │
                 │  - Light AI workloads         │
                 └──────────────┬────────────────┘
                                │
                                │
                 ┌──────────────┴───────────────┐
                 │     Dedicated AI Server      │
                 │  - Heavy model inference     │
                 │  - GPU expansion             │
                 │  - High-performance tasks    │
                 └──────────────┬───────────────┘
                                │
                                │  Tailscale Mesh Network
                                │
                 ┌──────────────┴───────────────┐
                 │     Workshop AI Server       │
                 │  - Edge compute              │
                 │  - Local inference           │
                 │  - CNC/3D printer logic      │
                 └──────────────────────────────┘
```

---

## Node Roles

### **Main TrueNAS Server**
- Primary storage for datasets and media  
- Runs Plex, Immich, Syncthing  
- Handles lightweight AI tasks  
- Acts as the central data source for the mesh  

### **Dedicated AI Server**
- Handles heavy model inference  
- Supports GPU upgrades  
- Runs isolated AI workloads without impacting storage performance  
- Ideal for large models and batch processing  

### **Workshop AI Server**
- Provides local compute for workshop tools  
- Handles edge inference for:
  - CNC workflows  
  - 3D printing  
  - Local automation  
- Reduces latency for workshop-specific tasks  

---

## How the Mesh Works

- All nodes communicate over **Tailscale**, forming a secure, encrypted mesh.  
- Models and datasets can be synced via:
  - Syncthing  
  - ZFS replication  
  - Manual deployment  
- Workloads can be distributed based on:
  - Location  
  - Latency  
  - Hardware capability  
  - Task type  

This creates a flexible, resilient compute environment that scales across physical spaces.

---

## Last Updated
May 2026
