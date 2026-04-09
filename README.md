<div align="center">



# 🛰️ OrionEye v4.0

### Cyber & Geospatial Intelligence Platform

[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-facelive.net-00e5ff?style=for-the-badge)](https://facelive.net/orioneye/)
[![Version](https://img.shields.io/badge/Version-4.0-blueviolet?style=for-the-badge)]()
[![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)]()

**Real-time cyber intelligence, geospatial analysis, space tracking, OSINT & AI orchestration.**\
**Built entirely by one developer. Powered by Gemini AI.**

[🚀 Live Demo](https://facelive.net/orioneye/) · [📸 Screenshots](#-screenshots) · [📖 Features](#-feature-overview) · [🏗️ Architecture](#%EF%B8%8F-architecture) · [👤 Author](#-author)

---

<table>
<tr>
<td align="center"><strong>20</strong><br><sub>Intelligence Modules</sub></td>
<td align="center"><strong>52</strong><br><sub>AI Tools</sub></td>
<td align="center"><strong>112+</strong><br><sub>Console Commands</sub></td>
<td align="center"><strong>30+</strong><br><sub>API Endpoints</sub></td>
<td align="center"><strong>18+</strong><br><sub>External APIs</sub></td>
<td align="center"><strong>2</strong><br><sub>Languages (EN/IT)</sub></td>
</tr>
</table>

</div>

---

## 📖 Feature Overview

OrionEye is a **full-stack intelligence platform** that combines network diagnostics, geospatial analysis, space tracking, OSINT tools and AI orchestration into a single interactive dashboard built on Google Maps.

### 🔒 Cyber Intelligence
| Module | Description |
|--------|-------------|
| **IP Geolocation** | Locate any IP address with ISP, ASN, city-level accuracy and map visualization |
| **Traceroute Visualization** | Visual network path tracing with hop-by-hop geolocation on the map |
| **DNS Lookup** | Full DNS resolution (A, AAAA, MX, NS, TXT, SOA, CNAME) |
| **Ping & Latency** | Real-time host reachability testing with structured RTT |
| **RIPE Atlas Probes** | Live map of RIPE NCC measurement probes worldwide |
| **RIPE AS/Prefix Info** | Autonomous System and IP prefix intelligence |
| **Network Builder** | Create custom network topologies (IX, datacenter, city nodes) with connections |
| **Spectrometer** | Network signal spectrum analyzer visualization |

### 🌍 Geospatial Intelligence
| Module | Description |
|--------|-------------|
| **Google Maps Integration** | Full interactive map with satellite, terrain, hybrid views |
| **Street View** | Immersive street-level exploration |
| **Route Planning** | Walking and driving route calculation with distance/time |
| **Traffic Cameras** | Live DOT traffic camera feeds on the map |
| **Weather Overlay** | Real-time weather data via Open-Meteo and Windy integration |
| **EV Charging Stations** | 550+ stations across 28 EU countries via OpenChargeMap API |

### 🛸 Space & Aerospace
| Module | Description |
|--------|-------------|
| **ISS Real-Time Tracker** | Live International Space Station position with orbit path |
| **ESA Rocket Launches** | Upcoming and past launches from all agencies (SpaceX, NASA, ESA, Roscosmos, JAXA...) |
| **Launch Pads** | Global launch sites mapped with details |
| **Space Stations** | Active and historical space station tracking |
| **Astronaut Database** | Current crew in space with bios |
| **Space Events** | Conferences, EVAs, dockings and space milestones |
| **Launch History** | Historical launch database with success/failure statistics |
| **OpenSky Aircraft** | Live aircraft tracking with ADS-B data |
| **CelesTrak Satellites** | Real-time satellite tracking (Starlink, GPS, weather, military...) |

### 🌐 OSINT & Intelligence
| Module | Description |
|--------|-------------|
| **NASA EONET** | Natural disaster events — wildfires, storms, earthquakes, volcanoes |
| **NASA GIBS Satellite** | Multi-layer satellite imagery (MODIS, VIIRS, Landsat) |
| **GDELT Conflicts** | Global conflict and protest monitoring |
| **ACLED Data** | Armed conflict tracking and analysis |
| **News Intelligence** | Real-time global news aggregation and search |
| **Facebook OSINT** | Public Facebook data monitoring and alerts |
| **RSS OSINT** | Custom RSS feed monitoring with keyword alerts |

### 💼 Job Intelligence
| Module | Description |
|--------|-------------|
| **Job Search** | Multi-platform job search (Adzuna, Remotive, JSearch) |
| **Salary Intelligence** | Salary estimation by role, location and experience |
| **Freelancer Discovery** | Find freelancers and contractors worldwide |

### 🎨 Visual Effects
| Effect | Description |
|--------|-------------|
| **NVG (Night Vision)** | Military-style green night vision filter |
| **FLIR (Thermal)** | Infrared thermal imaging simulation |
| **CRT** | Retro CRT monitor scanline effect |
| **Cyber** | Cyan cyberpunk neon overlay |

---

## 🤖 AI Integration

OrionEye features deep **Gemini AI** integration with **52 function-calling tools**. The AI can autonomously execute any platform command via natural language:

```
> "Show me all SpaceX launches this year"
> "Track the ISS and show me who's on board"  
> "Locate 8.8.8.8 and trace the route from my IP"
> "Find cybersecurity jobs in Berlin paying over 80k"
> "Show conflicts in Ukraine from the last 30 days"
> "Enable night vision and track military satellites"
> "Find EV charging stations near Munich"
```

The AI understands context, chains multiple tools together, and provides intelligence analysis on the results. **Voice output** is supported via Google TTS.

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────┐
│                     CLIENT (Browser)                     │
│  TypeScript · Google Maps JS API · Gemini AI · CSS VFX  │
└──────────────────────┬──────────────────────────────────┘
                       │ HTTPS
              ┌────────▼────────┐
              │   Nginx Proxy   │
              │  Let's Encrypt  │
              └────────┬────────┘
                       │
         ┌─────────────▼─────────────┐
         │    Node.js API Server     │
         │  30+ endpoints · Pino     │
         │  Rate Limiting · Cache    │
         └─────────────┬─────────────┘
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
  ┌──────────┐  ┌───────────┐  ┌──────────┐
  │  SQLite  │  │   Redis   │  │ External │
  │  Auth &  │  │   Cache   │  │   APIs   │
  │ Tracking │  │           │  │  (18+)   │
  └──────────┘  └───────────┘  └──────────┘
```

### Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Frontend** | TypeScript, Vite 4, Google Maps JavaScript API, CSS3 (custom VFX) |
| **Backend** | Node.js, Express-style HTTP server, Pino logging |
| **Database** | SQLite (better-sqlite3) — auth, sessions, visitor tracking |
| **Cache** | Redis, in-memory LRU cache |
| **AI** | Google Gemini 2.0 Flash — 52 function-calling tools |
| **Infrastructure** | Nginx, PM2, Let's Encrypt SSL, Ubuntu VPS |
| **Languages** | English, Italian (full i18n) |

### External APIs Integrated

| API | Purpose |
|-----|---------|
| Google Maps Platform | Maps, Geocoding, Directions, Street View |
| Google Gemini AI | Natural language AI with function calling |
| Google TTS | Voice synthesis for AI responses |
| Google Analytics 4 | Traffic analytics via Data API |
| NASA EONET | Natural disaster events |
| NASA GIBS | Satellite imagery layers |
| Launch Library 2 | Rocket launches worldwide |
| OpenSky Network | Live aircraft ADS-B tracking |
| CelesTrak | Satellite TLE orbital data |
| RIPE Atlas / RIPEstat | Network measurement probes and BGP data |
| GDELT | Global conflict event data |
| ACLED | Armed conflict database |
| NewsAPI | Global news aggregation |
| Adzuna | Job listings (multi-country) |
| Remotive | Remote job listings |
| OpenChargeMap | EV charging station network |
| ip-api | IP geolocation enrichment |
| Open-Meteo / Windy | Weather data and wind maps |

---

## 🖥️ Console Commands

OrionEye includes a **full command-line console** with 112+ commands. Examples:

```bash
# Network
ping google.com          # Ping a host
trace 1.1.1.1            # Visual traceroute
dns example.com          # DNS lookup
myip                     # Show your public IP
latency cloudflare.com   # Measure RTT

# Space
iss                      # Track the ISS live
launches                 # Upcoming rocket launches
astronauts               # Who's in space?
satellites starlink      # Track Starlink constellation
aircraft                 # Live aircraft radar

# Intelligence
news "climate change"    # Search global news
conflicts ukraine        # GDELT conflict data
events                   # NASA natural events
ripe probes IT           # RIPE Atlas probes in Italy
facebook alerts          # Facebook OSINT alerts

# Map & Visualization
vfx nvg                  # Night vision mode
vfx flir                 # Thermal imaging
streetview 48.8,2.3      # Paris Street View
route "Rome" "Milan"     # Route planning
charging                 # EV charging stations

# AI
ask "anything"           # Talk to Gemini AI
voice on                 # Enable voice output
lang it                  # Switch to Italian
```

---

## 📸 Screenshots

> **[🌐 Try the live demo →](https://facelive.net/orioneye/)**

<div align="center">

| Dashboard | ISS Tracking |
|:---------:|:------------:|
| *Main intelligence dashboard with interactive map* | *Real-time ISS orbit visualization* |

| Traceroute | Night Vision |
|:----------:|:------------:|
| *Visual hop-by-hop traceroute on world map* | *NVG military-style filter effect* |

</div>

---

## 🔐 Security & Privacy

- **GDPR Compliant** — Full privacy policy, cookie transparency, data subject rights
- **No Third-Party Tracking** — No Google Analytics cookies on the platform itself
- **Rate Limiting** — All API endpoints protected with configurable rate limits
- **Input Sanitization** — All user inputs validated and sanitized server-side
- **Secure Headers** — CORS, CSP, and security headers configured via Nginx
- **Auth System** — bcrypt/scrypt password hashing, JWT tokens, session management
- **No Data Selling** — Zero data shared with or sold to third parties

---

## 📄 Legal

- [Privacy Policy](https://facelive.net/orioneye/landing/privacy.html)
- [Terms of Service](https://facelive.net/orioneye/landing/terms.html)
- [Privacy Policy (Mobile)](https://facelive.net/orioneye/landing/privacy-mobile.html)
- [Privacy Policy (Simple IT)](https://facelive.net/orioneye/landing/privacy-simple.html)

---

## 👤 Author

<table>
<tr>
<td>

**Samuel La Manna**\
Software Engineer & Intelligence Architect

- 🌐 [facelive.net/orioneye](https://facelive.net/orioneye/)
- 📧 [privacy@facelive.net](mailto:privacy@facelive.net)
- 💼 [LinkedIn](https://www.linkedin.com/in/samuel-la-manna/)

</td>
</tr>
</table>

---

## ⚠️ Disclaimer

> This repository contains **documentation and information only** — no source code is published.\
> OrionEye is a proprietary project. All rights reserved © 2024–2026 Samuel La Manna.\
> The platform is intended for **educational and research purposes** in the fields of cybersecurity, geospatial intelligence, and network analysis.

---

<div align="center">

**Built with 🖤 by [Samuel La Manna](https://facelive.net/orioneye/)**

*One developer. 20 modules. 52 AI tools. Zero compromises.*

</div>
