# AetherChat — Anonymous Global P2P Chat (100% Frontend, Vercel-Ready)

AetherChat is a zero-backend, privacy-first anonymous global chatting web application engineered for instant static deployment on **Vercel**.

## Key Architecture Highlights

1. **100% Frontend Serverless Communication (`No Backend Required`)**:
   - **Global Serverless WebSocket Mesh**: Connects directly from the browser to public MQTT-over-WebSockets relay (`wss://broker.emqx.io:8084/mqtt`) and WebRTC/BroadcastChannel so users anywhere on the internet or across browser tabs can chat in real time without any custom backend or database.
   - **Automatic Sandbox & Offline Fallback**: If a corporate firewall or sandboxed environment restricts external WebSockets, AetherChat seamlessly falls back to local `BroadcastChannel` multi-tab sync + intelligent simulated global peers.

2. **Cryptographic Ephemeral Anonymity**:
   - Generates deterministic cryptographic aliases (`CipherFox#4821`, `NullSpecter#9012`) and Web Crypto SHA-256 session fingerprints entirely in memory.
   - **1-Click Burn Identity**: Instantly rotates your alias, avatar seed, and cryptographic fingerprint with zero cookies or tracking.

3. **Multi-Layer Client-Side Profanity & Toxicity Shield**:
   - **Lexical + Leetspeak + Obfuscation Engine**: Normalizes zero-width characters, symbol substitutions (`@`, `$`, `!`, `*`, `1`, `0`), repeated characters, and spaced-out evasions (`f u c k`) before any message leaves your browser.
   - **Configurable Enforcement**: Toggle between **Strict Block Mode** (blocks transmission and explains why) and **Auto-Sanitize Mask Mode** (replaces vulgar words with `[REDACTED]` or `****`), plus custom blocked word rules.

4. **Senior Software Engineer Technical SEO**:
   - Semantic HTML5 landmarks (`<header>`, `<main>`, `<nav>`, `<aside>`, `<section>`, `<article>`)
   - Complete Open Graph (`og:*`), Twitter Cards (`twitter:*`), Canonical URL, and `hreflang` tags
   - Dual Schema.org JSON-LD graphs (`WebApplication` + `FAQPage`)
   - Production `robots.txt`, `sitemap.xml`, `site.webmanifest`, and `vercel.json` edge headers

## Deploy to Vercel in 30 Seconds

### Method 1: Vercel CLI
```bash
npx vercel --prod
```

### Method 2: GitHub / Drag & Drop
1. Push this directory (`index.html`, `robots.txt`, `sitemap.xml`, `vercel.json`, `site.webmanifest`) to a GitHub repository.
2. Import the repository into [Vercel](https://vercel.com/new) with **Framework Preset: Other (Static)**.
3. Click **Deploy**.
