# 🎵 VIQ – Release Landing Page Generator
Internal tool to generate music release landing pages, ready to be uploaded to GitHub Pages in seconds.

---

## 🚀 Features

### 🛠 Generator
- **Auto-fill links** via the Odesli API — paste a Spotify (or other platform) link and all platform links are filled automatically
- **Cloudflare Worker proxy** — custom proxy for reliable API calls both locally and in production
- **12 supported platforms**: Spotify, Apple Music, YouTube, YouTube Music, Deezer, SoundCloud, Amazon Music, Tidal, Bandcamp, Pandora, Anghami, Store
- **Cover optimization** — automatic resize to 1000×1000px JPEG on import, with preview
- **Dominant color extraction** — the primary color of the cover is automatically extracted and injected into the landing page and OG image
- **Manual color override** — color picker displayed after cover upload, with reset button
- **OG image generation** — a 1200×630px image is automatically generated for Discord, Facebook, Twitter/X. Artist name adapts with word-wrap and letter-spacing for long names
- **Live preview** — the landing page and OG update in real time without regenerating
- **Full-screen preview** — button to view the landing page full-screen without the phone mockup
- **Auto slug** — generated from the song title, customizable
- **Final URL display** — `go.viqmusic.net/[slug]` shown with a one-click copy button
- **URL validation** — green/red visual indicator for each link
- **URL cleaning** — automatic removal of tracking parameters (utm, etc.) on blur
- **Config duplication** — clone a page while keeping artist + social links, clearing title + release links
- **ZIP export** — direct download on generate, no dialog. Generates a `[slug]/` folder containing `index.html`, `cover.jpg`, and `og.jpg`
- **Drag & drop** support for the cover area
- **Promo posts generator** — auto-generated TikTok and Facebook/Instagram captions based on the release info, editable before copying

---

### 🌐 Generated Landing Page
- **Animated particles** floating upward, tinted with the cover's primary color
- **Entry animation** on the cover (zoom + fade)
- **Parallax effect** on the cover when scrolling
- **Hover zoom** effect on the cover
- **Single column layout** — optimized for mobile, clean on all screen sizes
- **Dynamic background** — blurred cover in background with dark overlay
- **Artist name adaptive sizing** — font size and letter-spacing reduce automatically for long artist names
- **Share button** — native on mobile (Web Share API), link copy fallback
- **Social links** — Instagram, TikTok, Facebook, website
- **Favicon** = release cover
- **Full Open Graph tags** — `og:image`, `og:title`, `og:description`, `twitter:card`, `canonical`

---

### 🖼 OG Image
- Cover aligned to the right edge, softly faded on the left
- Background = blurred cover across the entire image
- Artist name large (serif) with smart word-wrap and adaptive letter-spacing for long names
- Title in light weight
- Decorative line in the primary color
- Release type in spaced lettering
- Gradient color bar at the bottom
- Subtle `viqmusic.net` domain at bottom left

---

## 📦 Generated ZIP Structure
```
[slug]/
├── index.html       # Complete landing page
├── cover.jpg        # Optimized 1000×1000 cover
└── og.jpg           # 1200×630 OG image for social sharing
```

---

## 🚀 Deployment
1. Generate the ZIP from the generator
2. Unzip and upload the `[slug]/` folder into the `releases` GitHub repository
3. The page goes live at: `https://go.viqmusic.net/[slug]`

---

## 🧠 Stack
Vanilla HTML / CSS / JavaScript
Zero server dependencies. Zero frameworks.

Libraries used:
- `JSZip` — client-side ZIP generation
- `Odesli API` via custom Cloudflare Worker — link auto-fill
- `SimpleIcons CDN` — platform logos

---

## ⚠️ License
© 2026 VIQ — All Rights Reserved.
