# CommanderPhu – Astro Page Design Guideline (v1.0)

## 1. Zweck der Astro-Page

Die Astro-Page ist das **digitale Command Center von CommanderPhu**.

Ziele:
- klare Identität vermitteln
- Vertrauen aufbauen
- zentrale Verlinkung zu Twitch, Projekten und K.I.T. Solutions
- ruhige, professionelle Präsenz

Nicht:
- Twitch-Overlay
- Social-Media-Feed
- Gaming-Landingpage

---

## 2. Markenrolle

CommanderPhu steht auf der Website für:
- Tech Creator
- IT Professional
- Builder & Thinker
- Gründer von K.I.T. Solutions

Tonalität:
- ruhig
- strukturiert
- technisch
- ehrlich

---

## 3. Seitenstruktur

Empfohlener Aufbau:

Header (minimal)  
Hero / Intro  
What I Do  
Projects / Tech  
Streaming / Content  
About / Philosophy  
Footer

Regeln:
- eine Hauptaussage pro Section
- klare Abstände
- kein visuelles Overloading

---

## 4. Farbkonzept

### Hintergrund
- Primary: #1F2933
- Secondary: #2E3440

### Text
- Headings: #F5F7FA
- Body: #D1D5DB
- Meta: #9AA5B1

### Akzent
- Commander Orange: #FF8C1A

Regel:
- Orange nur für Links, aktive States, Marker und CTAs
- kein Orange als Vollflächen-Hintergrund

---

## 5. Typografie

### Headings
- Orbitron oder Rajdhani SemiBold
- uppercase
- letter-spacing: 0.08em

### Body Text
- Inter oder Roboto

Priorität: Lesbarkeit vor Stil

---

## 6. Hero Section

Inhalt:
- Name
- Rolle
- ein klarer Satz

Beispiel:

COMMANDERPHU  
Tech Creator & IT Professional  

Building clean tech, streaming code and commanding systems.

CTAs:
- Twitch
- K.I.T. Solutions

Maximal 2 CTAs.

---

## 7. Content-Guidelines pro Section

### What I Do
- kurze Bulletpoints
- keine Buzzwords

Beispiel:
- Tech Streaming (Coding, Systems, Talk)
- IT & Infrastructure
- Creator-Focused Solutions
- Ethical & Open Tech

---

### Projects / Tech
Pro Projekt:
- Name
- Kurzbeschreibung
- Tech-Stack
- Link

Qualität vor Quantität.

---

### Streaming / Content
- wann du streamst
- was man erwarten kann
- warum du streamst

Kein Twitch-Hype, keine Emotes.

---

### About / Philosophy
Persönlich, aber ruhig.

Themen:
- Klarheit statt Chaos
- Technik als Werkzeug
- Nachhaltige IT
- Lernen & Teilen

---

## 8. Komponenten-Guideline

### Cards
- dunkler Hintergrund
- feine Border (rgba(255,255,255,0.06))
- keine harten Shadows

### Buttons
- transparent oder outlined
- Hover: Text oder Linie in Orange
- keine Orange-Vollflächen

### Icons
- Outline-Stil
- einfarbig
- keine Emojis

---

## 9. Animation & Motion

Erlaubt:
- Fade-In
- leichte Slide-Ins
- dezente Hover-Effekte

Nicht erlaubt:
- Bounce
- starke Parallax
- Scroll-Hijacking

Motion unterstützt den Inhalt – nicht umgekehrt.

---

## 10. Schreibstil

- ruhig
- direkt
- technisch verständlich
- ehrlich

Nicht:
- Marketing-Buzzwords
- Hustle-Sprache
- Clickbait

---

## 11. SEO & Meta

Title:
CommanderPhu – Tech Creator & IT Professional

Description:
Tech Creator, IT Professional and Founder of K.I.T. Solutions.
Streaming coding, building systems and sharing clean tech.

---

## 12. Do & Don’t

### Do
- Klarheit
- Struktur
- Ruhe
- Substanz

### Don’t
- Twitch-Optik auf der Website
- zu viele Farben
- zu viele Fonts
- visuelle Effekthascherei

---

## 13. Empfohlene Projektstruktur (Astro)

src/
layouts/
BaseLayout.astro
components/
Section.astro
Card.astro
Button.astro
Header.astro
pages/
index.astro
styles/
theme.css

---

## Versionierung

v1.0 – Initiale Design Guideline für CommanderPhu Astro-Page
