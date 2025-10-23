# 🧭 Homelab Project Roadmap

A living document outlining my ongoing and future homelab projects — covering infrastructure, automation, networking, monitoring, and experimental builds.  
This roadmap serves both as personal documentation and a public log of my self-hosted ecosystem.

---

## 🏠 Overview

| Category | Focus | Current Status |
|-----------|--------|----------------|
| Infrastructure | Core servers, virtualization, storage | ✅ Stable |
| Networking | VPN, DNS, reverse proxy, HTTPS | ⚙️ In Progress |
| Automation | Scheduling, orchestration, backups | 🧩 Planned |
| Media & Productivity | Media servers, photo management | ✅ Active |
| Security & Monitoring | Access control, uptime, telemetry | 🧩 Planned |

---

## 🗓️ Roadmap

### 🟢 Phase 1 — Current Stack
**Goal:** Maintain stability, certificates, and local networking integrity.

**Active Projects**
- [x] **TrueNAS SCALE** — ZFS storage, dataset management, and app deployment   
- [x] **Tailscale** — VPN mesh for secure remote access  
- [x] **Uptime-Kuma** — Uptime and service monitoring dashboard  
- [x] **Speedtest-Tracker** — Network performance visualization  
- [x] **Homepage** — Central dashboard for all homelab applications  
- [x] **Docmost** — Self-hosted documentation platform (Notion-style)  
- [x] **Calibre** — Ebook management and library server  
- [x] **Jellyfin + Jellyseerr + Jellystat** — Media server, request manager, and analytics suite  
- [x] **Mealie** — Recipe and meal planning platform  
- [x] **Prowlarr + Radarr + Sonarr + qBittorrent** — Full automation chain for media acquisition  
- [ ] **Caddy + Let’s Encrypt** — HTTPS reverse proxy and certificate management  
- [ ] **DuckDNS** — Dynamic DNS for external HTTPS validation  
- [ ] **AdGuard Home** — DNS-level ad and tracker blocking  
- [ ] **Dockpeek** ([repo](https://github.com/dockpeek/dockpeek)) — lightweight Docker container visibility dashboard  

---

### 🟡 Phase 2 — Short-Term Goals (Next 3–6 Months)
**Goal:** Improve automation, scheduling, and observability across the lab.

**Planned Projects**
- [ ] **Grafana + Prometheus** — centralized monitoring and metrics  
- [ ] **PiKVM** — headless hardware control over LAN  
- [ ] **ZFS Snapshot Replication** — automated local + offsite backup  
- [ ] **Dockge / Portainer** — visual Docker orchestration  
- [ ] **Cronmaster** ([repo](https://github.com/fccview/cronmaster)) — manage and visualize cron jobs via dashboard  
- [ ] **Tracktor** ([repo](https://github.com/javedh-dev/tracktor)) — container uptime and metrics tracker  
- [ ] **Immich + Immich-Drop** ([Immich](https://github.com/immich-app/immich), [Drop](https://github.com/Nasogaa/immich-drop)) — self-hosted photo and video backup with mobile sync  
- [ ] **Sprout Track** ([repo](https://github.com/Oak-and-Sprout/sprout-track)) — personal habit and activity tracker (potential for local hosting)  
- [ ] **AdventureLog** ([repo](https://github.com/seanmorley15/AdventureLog)) — self-hosted journal / activity logging app for family trips and projects  

---

### 🔵 Phase 3 — Long-Term Goals (6–12 Months)
**Goal:** Enhance resilience, automation, and long-term observability.

**Future Projects**
- [ ] **Proxmox or Docker Swarm migration** — expand virtualization capabilities  
- [ ] **External Reverse Proxy Node** — redundant Caddy endpoint for failover  
- [ ] **Sommelier** ([repo](https://wiki.serversatho.me/en/sommelierr)) — unified application launchpad and dashboard  
- [ ] **Centralized Syslog + ELK Stack** — system-wide logging and event tracing  
- [ ] **Ansible or Terraform automation** — full infrastructure-as-code deployment  
- [ ] **CI/CD Pipeline** — automated build and update pipeline (GitHub Actions → Docker registry)  

---

## 🧩 Experimental / Research Ideas
*(Ideas or projects I may explore later — stored here for future reference.)*

- [ ] **Pi-based SDR / APRS Node**
- [ ] **Self-hosted AI stack (Ollama, LM Studio, or LLaMA.cpp)**
- [ ] **Local weather station with Grafana dashboard**
- [ ] **Private Bitwarden / Vaultwarden instance**
- [ ] **Custom DNS heatmap visualization (ELK + GeoIP integration)**
- [ ] **Smart home hub (Home Assistant + MQTT broker)**

---

## 📊 Infrastructure Map (WIP)

| Node | Role | OS / Platform | Notes |
|------|------|----------------|-------|
| `truenas-main` | Primary NAS / app host | TrueNAS SCALE | ZFS, Docker backend |
| `vm-proxy` | Reverse proxy | Ubuntu Server + Caddy | HTTPS routing, DuckDNS |
| `vm-monitor` | Metrics + observability | Ubuntu Server + Grafana | Awaiting Phase 2 setup |
| `rpi-kvm` | Remote control | Raspberry Pi OS | For PiKVM access |
| `vm-automation` | Jobs & tasks | Ubuntu Server + Cronmaster | Will manage periodic jobs |

---

## 🧰 Toolchain & Stack

| Layer | Tools / Platforms |
|-------|-------------------|
| **Networking** | Tailscale, DuckDNS, AdGuard Home, Router DNS overrides |
| **Certificates & HTTPS** | Caddy, Let’s Encrypt, internal HTTPS enforcement |
| **Storage** | ZFS, TrueNAS SCALE datasets, snapshot replication |
| **Containers** | Docker, TrueCharts, Dockge / Portainer |
| **Monitoring** | Grafana, Prometheus, Tracktor (planned) |
| **Automation** | Cronmaster, Ansible (future), GitHub Actions |
| **Security** | VPN mesh (Tailscale), reverse proxy SSL validation |
| **User Experience** | Sommelier dashboard, Dockpeek, local landing page |

---

## 🪄 Notes to Self
- [ ] Audit and document backup verification schedule  
- [ ] Automate Caddy certificate renewals (internal + external)  
- [ ] Add DNS heatmap visualization into Grafana once ELK stack is deployed  
- [ ] Consider Docker Compose YAML repo standardization for all apps  
- [ ] Evaluate Immich’s GPU offload with TrueNAS SCALE Docker runtime  

---

## 🗒️ Changelog
| Date | Update |
|------|---------|
| 2025-10-23 | Initial roadmap created and populated with project list |
| YYYY-MM-DD | Added / updated project phases |

---

## 🧠 Inspiration & References
- [r/homelab](https://www.reddit.com/r/homelab/)  
- [Awesome Self-Hosted](https://github.com/awesome-selfhosted/awesome-selfhosted)  
- [TrueNAS Documentation](https://www.truenas.com/docs/)  
- [Grafana Labs Tutorials](https://grafana.com/tutorials/)  
- [ServersAtHome Wiki](https://wiki.serversatho.me/en/sommelierr)

---

> _"A homelab isn’t just a network — it’s a living experiment."_  
> — **Xidney Salvosa**
