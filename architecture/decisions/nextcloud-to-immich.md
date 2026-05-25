# Architecture Evolution: Nextcloud → Immich + Syncthing → OllamaPool

## Overview
This document explains the architectural transition from a Nextcloud‑based storage and sync system to a more efficient, modular setup using Immich, Syncthing, and a repurposed storage pool for AI compute workloads (OllamaPool). It also covers the addition of a dedicated 5TB external HDD for family mobile‑device backups.

This evolution reflects a shift toward performance, reliability, and intentional system design.

---

## 1. Original Architecture: Nextcloud‑Centric Design

### **Purpose**
Nextcloud originally served as the all‑in‑one solution for:
- File sync  
- Mobile photo backup  
- Remote access  
- Family storage  
- General cloud functionality  

### **Limitations Discovered**
- Slow and unreliable mobile photo uploads  
- Heavy resource usage  
- Complex maintenance  
- Overlapping features with better tools  
- Monolithic design that didn’t match your modular philosophy  

---

## 2. Phase 1: Transition to Immich + Syncthing

### **Why Immich?**
Immich provided:
- Faster photo/video uploads  
- Better metadata handling  
- Automatic deduplication  
- A modern UI  
- A purpose‑built media pipeline  

### **Why Syncthing?**
Syncthing offered:
- Lightweight file sync  
- Peer‑to‑peer reliability  
- No central server dependency  
- Perfect fit for family devices  
- Better performance than Nextcloud Files  

### **Result**
Nextcloud’s responsibilities were cleanly split into:
- **Immich** → media backup + management  
- **Syncthing** → file sync + device‑to‑device backup  

This improved performance, reliability, and clarity.

---

## 3. Phase 2: Repurposing the Nextcloud Pool → OllamaPool

### **Reasoning**
Once Nextcloud was removed, its dedicated storage pool became unused.  
Instead of letting it sit idle, it was repurposed into:

### **🧠 `OllamaPool`**
A dedicated storage pool for:
- LLM models  
- Embeddings  
- Model cache  
- AI compute artifacts  
- Future distributed compute workloads  

### **Benefits**
- Isolated I/O for AI workloads  
- Prevents fragmentation of family data  
- Cleaner architecture  
- Predictable performance for LLMs  
- Aligns with your long‑term AI compute mesh plans  

---

## 4. Phase 3: Adding a Dedicated 5TB External HDD

### **Purpose**
A new 5TB external HDD was added to serve as:
- Immich backup target  
- Syncthing backup target  
- Family mobile‑device backup storage  
- Redundant cold‑storage layer  

### **Why This Matters**
- Provides off‑pool redundancy  
- Protects family photos and files  
- Creates a clean separation between “live data” and “backup data”  
- Strengthens your disaster‑recovery posture  

---

## 5. Final Architecture After the Evolution

### **Media**
- Immich (primary)  
- 5TB HDD (backup)  

### **File Sync**
- Syncthing (primary)  
- 5TB HDD (backup)  

### **AI Compute**
- OllamaPool (repurposed from Nextcloud pool)  

### **Storage Layout**
- ZFS pools remain clean and purpose‑specific  
- Backups isolated from compute  
- Compute isolated from family data  

---

## 6. Why This Evolution Matters

This transition demonstrates:
- Real‑world architectural decision‑making  
- Ability to pivot based on performance and reliability  
- Understanding of storage design  
- Modular thinking  
- Practical IT engineering skills  
- A privacy‑first, family‑centric approach  

This is the kind of decision record that hiring managers love to see.

---

## Last Updated  
May 2026
