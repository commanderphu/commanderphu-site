# 🧪 CommanderPhu — Twitch & Creator Website  
*Flash-inspired. Tech-driven. Powered by Astro.*

<p align="center">
  <img src="https://img.shields.io/badge/Astro-252548?style=for-the-badge&logo=astro&logoColor=FDFDFD" />
  <img src="https://img.shields.io/badge/TailwindCSS-0f172a?style=for-the-badge&logo=tailwindcss&logoColor=38bdf8" />
  <img src="https://img.shields.io/badge/Docker-001e2b?style=for-the-badge&logo=docker&logoColor=1ea7e1" />
  <img src="https://img.shields.io/badge/Twitch-0d0d14?style=for-the-badge&logo=twitch&logoColor=cb7fff" />
  <img src="https://img.shields.io/badge/Spotify-0d1f0a?style=for-the-badge&logo=spotify&logoColor=1db954" />
  <img src="https://img.shields.io/badge/TypeScript-1e293b?style=for-the-badge&logo=typescript&logoColor=4aaeff" />
</p>

---

## ✨ Features

### 🎥 Twitch Integration
- Live Player (Embed)
- Live Status Panel  
- Twitch Chat Embed  
- Commander Commands Panel  
- Live Online/Offline Detection

### 🎧 Spotify Integration
- Now Playing Anzeige  
- Album Art  
- Live Refresh  
- Anbindung an phu-api-hub v2

### 🎛 UI + Design
- Flash/STAR Labs inspiriertes Interface  
- Neon/Hologram Effekte  
- Global Navigation  
- Neues Layoutsystem (BaseLayout)  
- Strukturierte Styles unter `src/styles/`

---

## 📁 Projektstruktur

```
src/
├── components/
│   ├── GlobalNav.astro
│   ├── Welcome.astro
│   └── twitch/
│       ├── TwitchPlayer.astro
│       ├── TwitchChat.astro
│       └── TwitchStatusPanel.astro
├── layouts/
│   └── BaseLayout.astro
├── pages/
│   ├── index.astro
│   ├── twitch.astro
│   ├── commands.astro
│   └── spotify.astro
└── styles/
    ├── global.css
    ├── hologram.css
    └── panels.css
```

---

## 🔧 Entwicklung

### Setup

```sh
pnpm install
pnpm run dev
```

Die Seite läuft unter:

```
http://localhost:4321
```

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

Spotify:
```
/v2/spotify
```

Twitch:
```
/v2/twitch/status
/v2/twitch/chat
```

---

## ⚡ Vision

CommanderPhu ist ein Creator Command Center —  
ein Hub für Streaming, Musik, Nerd Culture und High-Tech Design.  

Geplant:
- Realtime Dashboard  
- Twitch Overlay  
- Spotify WebSocket Push  
- Auto OG-Images  
- STAR Labs UI Effekte

---

## 📜 License

MIT License  
Branding © CommanderPhu
