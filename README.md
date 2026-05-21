# 🐉 HydraScaner · The Ultimate Scaner

[![GitHub release](https://img.shields.io/badge/version-1.0-brightgreen)](https://github.com/iAmINRaZ/HydraScaner)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Made with ❤️](https://img.shields.io/badge/made%20with-%E2%9D%A4%EF%B8%8F-red)](https://github.com/iAmINRaZ)
[![Offline Ready](https://img.shields.io/badge/offline-ready-success)](https://github.com/iAmINRaZ/HydraScaner)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/iAmINRaZ/HydraScaner)
![GitHub stars](https://img.shields.io/github/stars/iAmINRaZ/HydraScaner?style=social)

**HydraScaner** is a **browser‑based, offline‑capable** scanner that tests IPs, IP ranges, SNIs, domains, and CDNs with **20+ advanced features** – including multi‑port scanning, raw TCP/HTTP/HTTPS ping, UDP latency (via WebRTC), TLS handshake time, config injection, port knocking, geo‑spoof detection, and **automatic Clash / Sing‑Box / V2RayN config generation**.  

No installation, no server, no VPN required – just open the HTML file in any modern browser.

---

## 🌟 Key Features (20+)

| Category | Features |
|----------|----------|
| **Core Scanning** | 📡 PING (Direct+TCP+UDP) · 🔄 PAIR (IP×SNI) · ▶ MASS SCAN · 20‑port scanning (customizable) |
| **Network Intelligence** | 🔍 Enrich (ISP/ASN/Reality) · 📡 Raw TCP/HTTP pings · 📊 Latency stability sparkline · 🌡️ Heatmap over time · 🌍 Geo‑spoofing detector |
| **Security & Stealth** | 🕵️ Stealth mode (random delays + dummy traffic) · 🚪 Port knocking detector · 🛡️ TLS handshake time · 🧬 Config fingerprinting (detect Xray/Nginx/Cloudflare) |
| **Config Management** | 🔐 Config Editor · 💉 Config injector (upgrade existing configs) · 📦 Config merger (build Clash groups) · ⚔️ Config War Room (live comparison) |
| **AI & Automation** | 🧠 Natural language config builder (“fast gaming proxy below 100ms”) · 🔧 ADVANCED PING (20 features in one click) |
| **Exports & Backups** | 📎 CSV / TXT / JSON · ☁️ Clash (YAML) / Sing‑Box / V2RayN · ☁️ GitHub Gist backup/restore |
| **Usability** | 🌓 Light/Dark theme · ✅ Alive filter · 🔍 Real‑time filter · ⚙️ Port blacklist/whitelist · ⚡ Asymmetric scan (prioritise low‑latency pairs) |

---

## 🎯 What Can You Scan?

- **Individual IPs** (IPv4) – unlimited, but scanner limits to 200 per batch for performance.  
- **IP ranges** – CIDR (`185.143.232.0/22`) or hyphen (`185.143.232.1-185.143.232.254`).  
- **SNIs / Domains / CDNs** – any domain name (e.g., `snapp.ir`, `cloudflare.com`).  
- **Proxy configs** – VLESS, VMESS, Trojan links (one per line).  

---

## 🚀 How to Use – Step by Step

### 1. **Download & Open**
- Download `hydrascaner.html` from the repository.  
- Open it in any modern browser (Chrome, Firefox, Edge, Brave).  
- **No internet required after download** – works offline.

### 2. **Enter Your Targets**
- **IP addresses** textarea: paste IPs, ranges, or CIDRs (any delimiter).  
- **SNI / Domains** textarea: paste domain names or CDN hosts.  
- Leave empty to use default fallbacks.

### 3. **Choose a Scan Mode**
| Button | What it does | When to use |
|--------|--------------|--------------|
| ▶ START MASS SCAN | Full scan: direct ping + IP×SNI pair on 37 ports | Comprehensive analysis |
| 📡 PING (Direct only) | Tests each IP and SNI individually (HTTP/HTTPS/TCP) | Quick latency check |
| 🔄 PAIR (IP×SNI only) | Tests every IP with every SNI on 20 ports | Find best working combination |
| 🔧 ADVANCED PING (20 features) | Direct tests + TLS handshake, UDP, fingerprinting, heatmap, etc. | Deep intelligence |

### 4. **Read the Results Table**
Columns include:  
`IP`, `SNI`, `Port`, `TLS(ms)`, `HTTP(ms)`, `TCP(ms)`, `UDP(ms)`, `Mbps`, `Spark` (stability), `Ports`, `CDN`, `ISP`, `ASN`, `Engine`, `Spoof`, `Real` (Reality), `IR` (Iranian IP).

### 5. **Use Extra Features**
- **Enrich** – adds ISP, ASN, Reality flag.  
- **Speed Test** – measures download Mbps.  
- **Raw Pings** – re‑measures TCP/HTTP.  
- **Config Injector** – upgrades your existing configs with the fastest found IP/SNI.  
- **War Room** – live comparison of selected proxies.  
- **Export** – CSV, TXT, JSON, Clash, Sing‑Box, V2RayN.  
- **Backup/Restore** – save results to GitHub Gist.

---

## 🧪 Example Workflow

1. Paste these IPs: `185.143.233.122`, `2.17.251.98`, `104.66.70.133`  
2. Paste SNIs: `snapp.ir`, `cloudflare.com`, `arvancloud.com`  
3. Click **🔧 ADVANCED PING**  
4. Wait 10–20 seconds.  
5. Click **Enrich** to see ISP/ASN.  
6. Click **Speed Test** to get Mbps.  
7. Export the best results as Clash config.

---

## 🛠️ Advanced Features Explained (Simple)

| Feature | What it really does |
|---------|----------------------|
| **TLS handshake time** | Measures only the cryptographic handshake, not whole HTTP request. |
| **Neighbourhood scan** | Expands an IP to a /24 range and tests nearby IPs. |
| **Stability sparkline** | Shows a coloured bar (`🟢🟡🔴`) based on latency history. |
| **Config injector** | Replaces addresses in your configs with fastest alive IP/SNI. |
| **Natural language AI** | Type “fast gaming proxy below 100ms” – it finds the best match. |
| **Stealth mode** | Adds random delays and dummy requests to avoid DPI detection. |
| **Port knocking** | Tries sequence 80→443→8080 to find hidden open ports. |
| **Heatmap** | Saves latency history in localStorage, shows trend. |
| **War room** | Keeps selected proxies open and refreshes every 30 seconds. |
| **UDP latency** | Uses WebRTC STUN to estimate UDP ping. |
| **Geo‑spoofing detector** | Flags IPs that claim to be in Iran but have <10ms latency. |
| **Port blacklist** | Skips certain ports during PAIR scan. |
| **DNS over HTTPS** | Resolves domains to IPs via Cloudflare DNS. |
| **Config fingerprinting** | Reads `Server` header to identify proxy engine. |
| **Progressive speed test** | Stops after finding 3 proxies above 50 Mbps. |
| **Config merger** | Builds a Clash load‑balancing group from selected rows. |
| **Gist backup** | Saves your alive results to a private GitHub Gist. |
| **Asymmetric scan** | Prioritises testing low‑latency pairs first. |

---

## 📁 Repository Structure
HydraScaner/
├── hydrascan_ultimate.html # Single‑file application
├── README.md # This file
└── LICENSE # MIT License

text

---

## 🤝 Contributing & Support

- Found a bug? [Open an issue](https://github.com/iAmINRaZ/HydraScaner/issues)  
- Want a feature? Suggest it in [Discussions](https://github.com/iAmINRaZ/HydraScaner/discussions)  
- Contact me: [Telegram @iAmINRaZ](https://t.me/iAmINRaZ)  

---

## 📜 License

MIT License – free for personal and commercial use.  

---

## 🌐 Live Demo

You can try a **hosted version** (if you enable GitHub Pages):  
1. Go to repo **Settings → Pages**  
2. Set branch to `main` and folder to `/ (root)`  
3. Access `https://iAmINRaZ.github.io/HydraScaner/hydrascaner.html`

---

**Made with ❤️ by iAmINRaZ**  
*Scan smart*
