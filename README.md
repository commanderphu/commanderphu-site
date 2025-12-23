# CommanderPhu — Tech Creator & IT Professional
*Building clean tech, streaming code and commanding systems.*

<p align="center">
  <img src="https://img.shields.io/badge/Astro-252548?style=for-the-badge&logo=astro&logoColor=FDFDFD" />
  <img src="https://img.shields.io/badge/TailwindCSS-0f172a?style=for-the-badge&logo=tailwindcss&logoColor=38bdf8" />
  <img src="https://img.shields.io/badge/Docker-001e2b?style=for-the-badge&logo=docker&logoColor=1ea7e1" />
  <img src="https://img.shields.io/badge/Twitch-0d0d14?style=for-the-badge&logo=twitch&logoColor=cb7fff" />
  <img src="https://img.shields.io/badge/TypeScript-1e293b?style=for-the-badge&logo=typescript&logoColor=4aaeff" />
</p>

---

## 🎯 Über das Projekt

Die offizielle Website von **CommanderPhu** – Tech Creator, IT Professional und Gründer von [K.I.T. Solutions](https://kit-it-koblenz.de).

Fokus auf:
- Klarheit statt Chaos
- Nachhaltige IT
- Lernen & Teilen
- Ethical & Open Tech

---

## ✨ Features

### 🏠 Hauptseite
- Professionelle Hero Section mit Twitch Avatar
- "What I Do" – Übersicht der Tätigkeiten
- "Streaming & Content" – Infos zum Stream
- "Philosophy" – Persönliche Werte und Ansätze
- SEO-optimiert mit Meta-Tags

### 🎥 Twitch Dashboard
- **Live Status Panel** mit Avatar und Stream-Info
- **Realtime Chat** via WebSocket (`wss://api.intern.phudevelopement.xyz/ws`)
- **Recent Followers** (Top 5)
- **Game Box Art** (wenn live)
- **Viewer Graph** und Live Terminal
- **Clips Panel**
- Auto-Refresh alle 30 Sekunden

### 🎮 Commands Page
- Interaktive Command-Liste mit Such- und Filterfunktion
- 20+ Twitch-Commands in 4 Kategorien (Basic, Music, Flash, Fun)
- URL-Highlighting (`/commands?name=!flash`)

### 🎨 Design System
- **Farbschema:** #1F2933 (Primary), #2E3440 (Secondary), #FF8C1A (Orange Accent)
- **Typography:** Orbitron/Rajdhani (Headings), Inter/Roboto (Body)
- **Design-Guideline:** `docs/CommanderPhu_Astro_Design_Guideline.md`
- Ruhige, professionelle Ästhetik ohne visuelle Effekthascherei

---

## 📁 Projektstruktur

```
commanderphu-site/
├── docs/
│   ├── CommanderPhu_Astro_Design_Guideline.md
│   └── twitch-commands.md
├── src/
│   ├── components/
│   │   ├── GlobalNav.astro
│   │   └── twitch/modules/
│   │       ├── AutoRefresh.astro
│   │       ├── ChatPanel.astro
│   │       ├── ClipsPanel.astro
│   │       ├── GameBoxArt.astro
│   │       ├── LiveTerminal.astro
│   │       ├── Recent-Follower.astro
│   │       ├── StatusPanel.astro
│   │       └── ViewerGraph.astro
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   ├── twitch.astro
│   │   └── commands.astro
│   └── styles/
│       └── global.css
└── public/
    └── favicon.svg
```

---

## 🔧 Entwicklung

### Voraussetzungen
- Node.js 18+
- pnpm

### Setup

```sh
# Dependencies installieren
pnpm install

# Dev Server starten
pnpm run dev

# Mit Host-Flag (für Zugriff aus dem Netzwerk)
pnpm run dev -- --host
```

Die Seite läuft unter:
- **Local:** `http://localhost:4321`
- **Network:** `http://<deine-ip>:4321`

---

## 🚀 Deployment

Docker Build:

```sh
docker build -t commanderphu-site .
```

Docker Run:

```sh
docker run -p 4321:4321 commanderphu-site
```

Caddy Reverse Proxy:

```caddy
commanderphu.io {
    reverse_proxy commanderphu-site:4321
}
```

---

## 🛰 API Integration

Die Website nutzt die **PHU API Hub v2.0.0** unter `https://api.intern.phudevelopement.xyz`

### Endpoints

**Twitch:**
- `GET /twitch/` – Stream Status & User Info
- `GET /twitch/followers` – Recent Followers
- `GET /twitch/clips` – Latest Clips
- `WebSocket: wss://api.intern.phudevelopement.xyz/ws` – Live Chat & Events

**WebSocket Messages:**
- `overlay:ready` (Client → Server) – Signal nach Verbindung
- `twitch:chat` (Server → Client) – Neue Chat-Nachricht
- `now_playing` (Server → Client) – Aktueller Track
- `emotes:init` (Server → Client) – Twitch Emotes

**Andere:**
- `GET /websocket/info` – WebSocket-Dokumentation
- `GET /docs/json` – OpenAPI-Dokumentation

---

## 📜 License

MIT License
Branding & Content © CommanderPhu 2025

---

## 🔗 Links

- **Website:** [commanderphu.de](https://commanderphu.de) *(coming soon)*
- **Twitch:** [twitch.tv/commanderphu](https://twitch.tv/commanderphu)
- **K.I.T. Solutions:** [kit-it-koblenz.de](https://kit-it-koblenz.de)

---

## 📝 Changelog

### v2.0.0 (2025-12-22)
- ✨ Komplettes Redesign gemäß Design-Guideline v1.0
- 🎨 Neues Farbschema: #1F2933, #2E3440, #FF8C1A
- 🔤 Neue Typography: Orbitron/Rajdhani & Inter/Roboto
- 🏠 Neue Hauptseite mit Hero, What I Do, Streaming, Philosophy
- 🎥 Twitch Dashboard mit WebSocket-Chat
- 📊 Recent Followers Integration
- 🎮 Interaktive Commands Page
- 🔧 API-URLs auf `/twitch/` aktualisiert
- 📱 Responsive Design für alle Geräte
