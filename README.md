# 🎬 SanuFlix - Open Source Streaming Platform

<div align="center">

### 🌐 [Live Demo](https://sanuflix-web-v2.pages.dev/)

[![Deploy to Cloudflare Pages](https://img.shields.io/badge/Deploy-Cloudflare%20Pages-F38020?logo=cloudflare)](https://pages.cloudflare.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

</div>

---

> [!WARNING]
> **Legal Disclaimer**: This application does not host, store, or distribute any movies, TV shows, or copyrighted content. All video content is provided by **third-party embed servers** that are configured by the user. The developer is not responsible for any content accessed through this application. Use at your own risk and ensure compliance with your local laws.

---

## 🚀 Quick Start

### 1. Clone & Install

```bash
git clone https://github.com/Sanuu7/SanuFlix-opensource
cd sanuflix-opensource
npm install
```

### 2. Configure Environment

```bash
cp .env.example .env
```

Edit `.env`:

```env
# Required: Get free at https://themoviedb.org/settings/api
VITE_TMDB_API_KEY=your_tmdb_api_key_here

# Optional
VITE_SPORTS_API_URL=
VITE_APP_NAME=SanuFlix
VITE_LOGO_URL=
```

### 3. Configure Streaming Servers

Edit `src/config/servers.ts` with your embed server URLs:

```typescript
export const STREAMING_SERVERS: StreamingServer[] = [
  {
    id: 'server1',
    name: 'Server 1',
    description: 'Primary streaming server',
    isActive: true,
    movieUrlTemplate: 'https://your-embed.example/movie/{tmdbId}',
    tvUrlTemplate: 'https://your-embed.example/tv/{tmdbId}/{season}/{episode}',
  },
]
```

### 4. Run Locally

```bash
npm run dev
```

---

## ☁️ Deploy to Cloudflare Pages

### Option 1: Direct GitHub Integration (Recommended)

1. Push your configured repo to GitHub
2. Go to [Cloudflare Pages Dashboard](https://dash.cloudflare.com/?to=/:account/pages)
3. Click **Create a project** → **Connect to Git**
4. Select your repository
5. Configure build settings:
   - **Framework preset**: `Vite`
   - **Build command**: `npm run build`
   - **Build output directory**: `dist`
6. Add environment variables:
   - `VITE_TMDB_API_KEY` = your TMDB key
7. Click **Save and Deploy**

### Option 2: Wrangler CLI

```bash
# Install Wrangler
npm install -g wrangler

# Login to Cloudflare
wrangler login

# Build the project
npm run build

# Deploy
wrangler pages deploy dist --project-name=sanuflix
```

---

## ✨ Features

- 🎨 Modern UI with Tailwind CSS
- 📱 PWA - Installable on any device
- 🎭 Multiple color themes
- 🔍 Search movies & TV shows
- 📺 Multi-server support
- ⚡ Fast with Vite + React

## 🛠 Tech Stack

React 18 • TypeScript • Vite • Tailwind CSS • Framer Motion

## 📁 Key Configuration Files

| File | Purpose |
|------|---------|
| `.env` | API keys |
| `src/config/servers.ts` | Embed server URLs |
| `src/config/themes.ts` | Color themes |

## 📋 Scripts

```bash
npm run dev      # Development
npm run build    # Production build
npm run preview  # Preview build
npm run lint     # Lint code
```

---

## ⚖️ License

This project is licensed under the [MIT License](./LICENSE).

---

<div align="center">

**Made with ❤️ by [Sanuu](https://github.com/Sanuu7)**

</div>
