# Security Mesh Architecture

This diagram outlines the fully local, privacy-first home security system built using ESP32-S3 camera modules, a Raspberry Pi hub, and a dedicated security backup server. It shows how events flow through the system and how redundancy is maintained without relying on any cloud services.

---

## Diagram: Security Mesh

```
                   ┌───────────────────────────┐
                   │      ESP32-S3 Cameras     │
                   │  - Motion detection       │
                   │  - Snapshots / clips      │
                   │  - Low-power nodes        │
                   └──────────────┬────────────┘
                                  │  WiFi / ESP-NOW
                                  │
                     ┌────────────┴─────────────┐
                     │     Raspberry Pi Hub     │
                     │  - Event ingestion       │
                     │  - Local AI detection    │
                     │  - Short-term storage    │
                     │  - Routing to backup     │
                     └────────────┬─────────────┘
                                  │
                                  │  ZFS Replication / Sync
                                  │
                     ┌────────────┴─────────────┐
                     │  Security Backup Server  │
                     │  - Long-term retention   │
                     │  - Encrypted datasets    │
                     │  - Redundant storage     │
                     └──────────────────────────┘
```

---

## Component Roles

### **ESP32-S3 Cameras**
- Capture snapshots and short video clips  
- Perform lightweight motion detection  
- Communicate via WiFi or ESP-NOW  
- Extremely low power and inexpensive to scale  

### **Raspberry Pi Security Hub**
- Central ingestion point for all camera events  
- Runs local AI models for:
  - Person detection  
  - Object detection  
  - Motion classification  
- Stores short-term footage  
- Forwards important events to the backup server  

### **Security Backup Server**
- Stores long-term security footage  
- Uses encrypted ZFS datasets  
- Provides redundancy against:
  - SD card corruption  
  - Pi failure  
  - Network outages  
- Can replicate to off-site storage if desired  

---

## Event Flow

1. **Camera detects motion**  
2. ESP32-S3 sends snapshot/clip to the Pi Hub  
3. Pi Hub runs local AI detection  
4. If event is important → send to Backup Server  
5. Backup Server stores encrypted long-term copy  

No cloud.  
No external dependencies.  
Fully sovereign.

---

## Key Advantages

- **Privacy-first**: All processing and storage stay local  
- **Redundant**: Backup server protects against Pi or SD card failure  
- **Low-power**: ESP32-S3 nodes are extremely efficient  
- **Scalable**: Add more cameras without major cost  
- **AI-enhanced**: Local detection reduces false positives  

---

## Last Updated
May 2026
