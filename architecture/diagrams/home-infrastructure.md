# Home Infrastructure Overview

This diagram provides a top-level view of the entire home-lab ecosystem, including servers, VLANs, IoT devices, workshop nodes, and distributed smart-home components. It serves as the primary reference for understanding how all major systems connect and interact.

---

## Diagram: Full Home Infrastructure

```
                          ┌──────────────────────────────┐
                          │        Internet / ISP        │
                          └───────────────┬──────────────┘
                                          │
                               ┌──────────┴───────────┐
                               │ Main Router/Firewall │
                               └──────────┬───────────┘
                                          │
                     ┌────────────────────┼──────────────────────┐
                     │                    │                      │
             ┌───────┴───────┐    ┌───────┴───────┐      ┌───────┴────────┐
             │   Main LAN    │    │   IoT VLAN    │      │  Workshop VLAN │
             └───────┬───────┘    └───────┬───────┘      └────────┬───────┘
                     │                    │                       │
     ┌───────────────┼───────────────┐    │                       │
     │                               │    │                       │
┌────┴────┐                    ┌─────┴────┐              ┌────────┴────────┐
│ TrueNAS │                    │ ESP32-S3 │              │  Workshop AI    │
│  Server │                    │ Repeaters│              │    Server       │
└────┬────┘                    └─────┬────┘              └────────┬────────┘
     │                               │                            │
     │                               │                            │
┌────┴──────────────┐       ┌────────┴────────┐         ┌─────────┴────────┐
│Dedicated AI Server│       │ ESP32-S3 Cameras│         │ Workshop Devices │
└────┬──────────────┘       └────────┬────────┘         └──────────────────┘
     │                                │
     │                                │
┌────┴───────────────┐       ┌────────┴────────┐
│ Backup Server      │       │ Pi Security Hub │
└────────────────────┘       └────────┬────────┘
                                       │
                                       │
                             ┌─────────┴─────────┐
                             │ ESP32-S3 Intercom │
                             └─────────┬─────────┘
                                       │
                                       │
                          ┌────────────┴────────────┐
                          │     Smart Lighting      |
                          └─────────────────────────┘
```

---

## Key Concepts

- **Main LAN**  
  Hosts core servers: TrueNAS, Dedicated AI Server, Backup Server.

- **IoT VLAN**  
  Contains ESP32-S3 devices: cameras, intercom, smart lighting, repeaters.

- **Workshop VLAN**  
  Houses the Workshop AI Server and any workshop-specific devices.

- **ESP32-S3 Repeaters**  
  Extend wireless coverage for cameras, lighting, intercom, and Pi nodes.

- **Security Mesh**  
  ESP32-S3 cameras → Pi Security Hub → Backup Server.

- **Compute Mesh**  
  TrueNAS Server → Dedicated AI Server → Workshop AI Server.

---

## Last Updated
May 2026
