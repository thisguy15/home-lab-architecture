# Future Improvements

This document outlines planned upgrades, enhancements, and long-term goals for the home-lab. These improvements focus on reliability, scalability, privacy, and hands-on learning.

---

## Storage & TrueNAS Enhancements

### **Add SSD Cache or Metadata Drives**
- Improve read/write performance
- Reduce latency for Plex, Immich, and Syncthing
- Extend HDD lifespan by reducing random writes

### **Expand Storage Pools**
- Add additional HDDs for larger media libraries
- Improve redundancy (RAIDZ2 or mirrored vdevs)
- Prepare for long-term family photo/video growth

---

## Networking Improvements

### **Refine VLAN Segmentation**
- Separate IoT, media, and admin networks
- Improve security and reduce broadcast noise
- Prepare for future smart home expansion

### **Add a Dedicated Router or Firewall**
- Move away from ISP router limitations
- Gain better control over:
  - DHCP reservations
  - Firewall rules
  - VLANs
  - Monitoring

---

## Tailscale & Remote Access

### **Enable a Dedicated Exit Node**
- Provide secure browsing for remote family members
- Centralize network egress for consistency

### **Add ACL Rules**
- Fine-tune which devices can talk to each other
- Improve security without adding complexity

---

## Raspberry Pi Projects

### **Improve Car Pi Audio Server**
- Add better power filtering
- Explore faster boot optimizations
- Add offline media sync automation

### **Add More Service Nodes**
- Pi-hole or AdGuard Home
- Lightweight automation services
- Local dashboards or monitoring tools

---

## Monitoring & Observability

### **Add Grafana + Prometheus**
- Track system performance
- Monitor:
  - CPU
  - RAM
  - Disk usage
  - Network throughput
- Create dashboards for long-term trends

### **Add Alerting**
- Email or mobile alerts for:
  - Disk failures
  - High CPU usage
  - Offline devices

---

## Documentation Goals

### **Add Architecture Diagrams**
- Visual diagrams for:
  - Network layout
  - Storage pools
  - Service relationships

### **Add Setup Guides**
- Step-by-step instructions for:
  - TrueNAS apps
  - Tailscale setup
  - Raspberry Pi provisioning

---

## Long-Term Vision
- Build a reliable, privacy-first infrastructure for my family  
- Continue learning system administration and networking  
- Expand into automation, monitoring, and multi-site connectivity  
- Maintain documentation that reflects real-world IT experience  
