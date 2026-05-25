# 🌐 Aqsa Zam Zam Mirza Johar Baig — Official Personal Brand Website
### *The complete guide to the personal profile website featuring the **Alerto Telegram Bot***

---

## 📌 Project Overview

This is the **official personal branding and portfolio website** for **Aqsa Zam Zam Mirza Johar Baig**, developer and creator of **Alerto** — an intelligent Telegram market bot for real-time stock prices, cryptocurrency tracking, price alerts, technical analysis, and live portfolio watchlists.

The website is designed to:
1. **Rank #1 on Google** for the keyword `Aqsa Zam Zam Mirza Johar Baig`
2. **Showcase Alerto** — its full feature set, every command, and technical architecture
3. **Establish professional credibility** with a premium, modern design

---

## 📂 Project File Structure

```
Alerto/
│
├── index.html          ← 🌟 Main website (single-file, all CSS internal)
├── robots.txt          ← Search engine crawler instructions
├── sitemap.xml         ← XML sitemap for all page sections
├── README.md           ← This guide
│
├── core/               ← Bot core config & logging
│   ├── config.py
│   └── logger.py
│
├── handlers/           ← Telegram command handlers
│   ├── start.py        (/ start — user registration + welcome)
│   ├── help.py         (/help — full command reference)
│   ├── price.py        (/price — stock price lookup)
│   ├── crypto.py       (/crypto — cryptocurrency prices)
│   ├── alerts.py       (/setalert, /alerts, /deletealert)
│   ├── watchlist.py    (/addstock, /removestock, /watchlist)
│   ├── stream.py       (/livewatchlist, /stoplive)
│   ├── technical.py    (/technical, /chart)
│   ├── fundamentals.py (/analyze, /fundamental)
│   ├── reports.py      (/hourly_report)
│   ├── search.py       (/search)
│   ├── cmd.py          (/cmd — command keyboard)
│   ├── ping.py         (/ping)
│   ├── keyboard.py     (reply keyboard builder)
│   └── error_handler.py
│
├── services/           ← Business logic & data providers
│   ├── database.py
│   ├── user_repository.py
│   ├── alert_repository.py
│   ├── alert_service.py
│   ├── watchlist_repository.py
│   ├── technical_service.py
│   ├── user_settings.py
│   ├── stream_manager.py
│   └── market/
│       ├── router.py           (smart market routing)
│       ├── stock_provider.py   (Yahoo Finance)
│       ├── crypto_provider.py  (CoinGecko)
│       ├── symbol_resolver.py  (auto-detect markets)
│       ├── cache.py            (TTL caching layer)
│       └── base.py
│
├── models/             ← Data models / schemas
│   ├── user.py
│   ├── alert.py
│   ├── watchlist.py
│   ├── market.py
│   ├── technical.py
│   └── fundamentals.py
│
├── utils/              ← Formatters, decorators, helpers
├── webapp/             ← Telegram Web App (visual watchlist)
│   ├── index.html
│   ├── style.css
│   └── app.js
│
├── data/               ← SQLite database (auto-created)
└── logs/               ← Rotating log files (auto-created)
```

---

## 🌍 Website Sections (index.html)

The website is a **single HTML file** with all CSS embedded. Here is the full section guide:

| # | Section ID | Content | SEO Purpose |
|---|-----------|---------|-------------|
| 1 | `#hero` | Name, role, Alerto badge, stats | Primary H1 keyword placement |
| 2 | `#about` | Bio, detail cards, quote | Secondary keyword reinforcement |
| 3 | `#alerto` | Bot overview + live terminal demo | Alerto project showcase |
| 4 | `#features` | 6 feature cards with commands | Feature discoverability |
| 5 | `#how-it-works` | 4-step getting started guide | UX + indexed content |
| 6 | `#commands` | Full command reference table (18+ cmds) | Rich structured content |
| 7 | `#tech` | Technology stack grid | Authority signals |
| 8 | `#biography` | Timeline: foundations → Alerto launch | E-E-A-T signals |
| 9 | `#faq` | 7 detailed Q&As (schema-marked) | FAQ rich snippets |
| 10 | `#contact` | All social + Telegram links | Engagement + entity building |

---

## 🔍 SEO Features Implemented

### Meta Tags
- ✅ Optimized `<title>` with primary keyword + Alerto
- ✅ `meta description` (155 chars, keyword-natural)
- ✅ `meta keywords` (primary + long-tail variations)
- ✅ `robots` with full crawl directives
- ✅ `canonical` URL
- ✅ `theme-color`, `color-scheme`, `language`, `geo.region`

### Open Graph & Social
- ✅ `og:type`, `og:title`, `og:description`, `og:image`, `og:url`
- ✅ `profile:first_name`, `profile:last_name`
- ✅ Full Twitter Card (summary_large_image)

### Schema Markup (JSON-LD)
- ✅ **Person** schema — full profile with `knowsAbout`, `sameAs`, `jobTitle`
- ✅ **SoftwareApplication** schema — Alerto bot with `featureList`, `creator`, `programmingLanguage`
- ✅ **WebSite** schema with `SearchAction`
- ✅ **WebPage** schema with `breadcrumb`
- ✅ **BreadcrumbList** schema (5 items)
- ✅ **FAQPage** schema (7 Q&As) — enables Google FAQ rich results

### Performance
- ✅ Fonts loaded non-blocking (`media="print"` swap trick)
- ✅ `preconnect` + `dns-prefetch` for Google Fonts
- ✅ Inline CSS — zero external CSS requests
- ✅ Zero JavaScript (pure CSS animations + checkbox accordion)
- ✅ SVG favicon inlined — zero icon HTTP request
- ✅ `clamp()` for fluid typography — no layout shifts
- ✅ `content-visibility` friendly structure

### Accessibility (WCAG 2.1 AA)
- ✅ Skip to main content link
- ✅ `aria-label` on all interactive elements
- ✅ `role` attributes (banner, main, navigation, contentinfo)
- ✅ Semantic HTML5 (`<header>`, `<main>`, `<section>`, `<article>`, `<nav>`, `<footer>`)
- ✅ `aria-hidden` on decorative elements
- ✅ `:focus-visible` styles for keyboard navigation
- ✅ `prefers-reduced-motion` media query support

---

## 🤖 Alerto Bot — Complete Feature Reference

### Supported Commands

| Command | Description |
|---------|-------------|
| `/start` | Register account + show keyboard menu |
| `/help` | Full command reference (admin section included for admins) |
| `/cmd` | Show reply keyboard of all commands |
| `/ping` | Check bot latency |
| `/price <symbol>` | Real-time stock price (US/NSE/BSE/global) |
| `/crypto <symbol>` | Live cryptocurrency price via CoinGecko |
| `/search <query>` | Find ticker symbol by company/coin name |
| `/setalert <sym> <above\|below\|drop\|rise> <value>` | Set price alert |
| `/alerts` | List all active alerts |
| `/deletealert <id>` | Remove an alert by ID |
| `/addstock <symbol>` | Add asset to watchlist (max 20) |
| `/removestock <symbol>` | Remove from watchlist |
| `/watchlist` | View watchlist with live prices |
| `/livewatchlist` | Start 10-second live streaming updates |
| `/stoplive` | Stop live stream |
| `/technical <symbol>` | Technical analysis (RSI, MACD, BB, AI insight) |
| `/chart <symbol>` | ASCII sparkline chart (30-day) |
| `/analyze <symbol>` | Fundamental analysis (P/E, EPS, mkt cap, etc.) |
| `/fundamental <symbol>` | Alias for `/analyze` |
| `/hourly_report on\|off\|status` | Toggle scheduled hourly reports |

### Supported Markets
- 🇺🇸 **US Stocks**: NYSE, NASDAQ (e.g., `AAPL`, `TSLA`, `GOOGL`)
- 🇮🇳 **Indian Stocks**: NSE (`.NS` suffix) and BSE (`.BO` suffix) (e.g., `RELIANCE.NS`, `TCS.BO`)
- 📈 **Global Indices**: S&P 500 (`^GSPC`), NIFTY 50 (`NIFTY50.NS`), etc.
- 💰 **All Crypto**: via CoinGecko (BTC, ETH, SOL, DOGE, SHIB, etc.)
- 🏅 **ETFs**: Gold ETFs, index ETFs (e.g., `GOLDBEES.NS`)

---

## 🛠️ Tech Stack (Alerto Bot)

| Technology | Purpose |
|-----------|---------|
| Python 3.12 | Core language |
| python-telegram-bot (async) | Bot framework |
| SQLite + aiosqlite | Persistent user data, alerts, watchlists |
| Yahoo Finance (yfinance) | Stock & index data |
| CoinGecko API | Cryptocurrency data |
| Metals API | Commodities data |
| APScheduler | Alerts engine + scheduled reports |
| pandas + TA-Lib | Technical indicator calculations |
| asyncio | Full async concurrency |
| Rotating file logs | Monitoring & debugging |
| Telegram Web App | Visual watchlist interface |

---

## 🚀 Deployment Guide

### Step 1 — Choose Your Domain
Register one of these recommended domains:
- `aqsazamzammirzajoharbaig.com` ⭐ (best for keyword ranking)
- `aqsabaig.com`
- `aqsamirza.dev`
- `aqsazamzam.me`

### Step 2 — Deploy the Website

#### Option A: GitHub Pages (Free)
```bash
# 1. Create a new GitHub repository: aqsazamzammirzajoharbaig.github.io
# 2. Upload index.html, robots.txt, sitemap.xml
# 3. Enable Pages in Settings → Pages → Deploy from branch (main)
# 4. Point your custom domain to GitHub Pages
```

#### Option B: Netlify (Free, Recommended)
```bash
# 1. Go to netlify.com → "Add new site" → "Deploy manually"
# 2. Drag and drop your project folder
# 3. Add custom domain in Site Settings → Domain Management
# 4. Netlify provides free SSL automatically
```

#### Option C: Vercel (Free)
```bash
# 1. Install Vercel CLI: npm i -g vercel
# 2. In the project folder: vercel
# 3. Follow prompts, add custom domain in Vercel Dashboard
```

#### Option D: AWS S3 + CloudFront
```bash
# 1. Create S3 bucket: aqsazamzammirzajoharbaig.com
# 2. Enable static website hosting
# 3. Upload all files
# 4. Create CloudFront distribution for HTTPS + CDN
# 5. Point domain to CloudFront
```

### Step 3 — Update Domain References
Before deploying, replace all occurrences of the placeholder domain in `index.html`:
```
https://aqsazamzammirzajoharbaig.com/
```
Change to your actual domain if different.

### Step 4 — Add Your Photo
Replace the emoji avatar `🌸` in the `hero-avatar` div with your actual profile photo:
```html
<!-- Replace this: -->
<div class="hero-avatar">🌸</div>

<!-- With this: -->
<img class="hero-avatar" 
     src="/your-photo.jpg" 
     alt="Aqsa Zam Zam Mirza Johar Baig — Profile Photo"
     width="400" height="400" />
```

### Step 5 — Update Bot Link
Replace `@AlertoMarketBot` with your actual Telegram bot username in all links.

### Step 6 — Submit to Google
1. Go to [Google Search Console](https://search.google.com/search-console)
2. Add your domain property
3. Submit `sitemap.xml`:
   ```
   https://yourdomain.com/sitemap.xml
   ```
4. Request indexing for the main URL

---

## 📊 SEO Keyword Strategy

### Primary Keyword (Target #1 Ranking)
```
Aqsa Zam Zam Mirza Johar Baig
AQSA ZAM ZAM MIRZA JOHAR BAIG
```

### Long-tail Keywords (Bonus Traffic)
```
Aqsa Zam Zam Mirza Johar Baig developer
Aqsa Zam Zam Mirza Johar Baig Alerto bot
Alerto Telegram market bot
Alerto bot price alerts
Alerto bot technical analysis
Aqsa Mirza Baig
Aqsa Johar Baig
```

### Keyword Placement Map (in index.html)
| Location | Keyword Used | ✅ |
|----------|-------------|---|
| `<title>` tag | Full name | ✅ |
| `meta description` | Full name | ✅ |
| `meta keywords` | Multiple variants | ✅ |
| `<h1>` (hero-name) | Full name | ✅ |
| First `<p>` of hero | Full name in bold | ✅ |
| `<h2>` About | Full name | ✅ |
| `<h2>` Biography | Full name | ✅ |
| `<h2>` Achievements | Full name | ✅ |
| All FAQ answers | Name mentioned | ✅ |
| Footer copyright | Full name | ✅ |
| Footer SEO text | Full name | ✅ |
| `og:title` | Full name | ✅ |
| `twitter:title` | Full name | ✅ |
| JSON-LD `Person.name` | Full name | ✅ |
| JSON-LD `alternateName` | 4 variants | ✅ |
| `aria-label` attributes | Full name | ✅ |
| Breadcrumbs | About, Alerto sections | ✅ |

---

## 🔧 Customization Guide

### How to Update Your Bio
Edit the `#about` section paragraphs in `index.html` (search for `about-content`).

### How to Add Your Real Photo
See Step 4 in the Deployment Guide above.

### How to Change Colors
Edit the CSS variables in `:root` at the top of the `<style>` block:
```css
:root {
  --clr-primary:   #a374ff;   /* Purple — change to your brand color */
  --clr-secondary: #f5a623;   /* Gold */
  --clr-teal:      #4ecdc4;   /* Teal (Alerto accent) */
}
```

### How to Update Bot Username
Search and replace `AlertoMarketBot` with your actual bot username across `index.html`.

### How to Add More FAQ Items
Copy a `.faq-item` block and increment the checkbox ID (`faq8`, `faq9`, etc.). Also add to the JSON-LD FAQPage schema in the `<head>`.

---

## 📋 robots.txt Reference

```
# Robots.txt — Aqsa Zam Zam Mirza Johar Baig Official Website

User-agent: *
Allow: /

Sitemap: https://aqsazamzammirzajoharbaig.com/sitemap.xml

Crawl-delay: 1
```

---

## 🗺️ Sitemap Sections (sitemap.xml)

| URL | Priority | Purpose |
|-----|----------|---------|
| `/` | 1.0 | Main homepage |
| `/#about` | 0.9 | About section |
| `/#alerto` | 0.95 | Alerto bot overview |
| `/#features` | 0.9 | Bot features |
| `/#commands` | 0.85 | Command reference |
| `/#how-it-works` | 0.8 | Getting started |
| `/#tech` | 0.75 | Tech stack |
| `/#biography` | 0.8 | Biography timeline |
| `/#faq` | 0.85 | FAQ (rich results) |
| `/#contact` | 0.7 | Contact info |

---

## ✅ Checklist Before Going Live

- [ ] Replace `aqsazamzammirzajoharbaig.com` with your actual domain
- [ ] Add your real profile photo (replace `🌸` emoji)
- [ ] Update `@AlertoMarketBot` with actual bot username
- [ ] Update social media links (LinkedIn, GitHub, Twitter, Instagram)
- [ ] Update email: `hello@aqsazamzammirzajoharbaig.com`
- [ ] Upload to hosting (Netlify / GitHub Pages / Vercel)
- [ ] Verify SSL is active (HTTPS)
- [ ] Submit to Google Search Console
- [ ] Submit sitemap.xml to Google
- [ ] Submit to Bing Webmaster Tools
- [ ] Add site to Google My Knowledge Panel (if applicable)
- [ ] Share link on LinkedIn with your full name in the post

---

## 🏗️ Architecture Decisions

| Decision | Rationale |
|----------|-----------|
| Pure HTML + CSS (no JS) | Maximum performance, no render-blocking scripts |
| Internal CSS only | Zero external CSS requests, instant rendering |
| Checkbox accordion (CSS) | Interactive FAQ without any JavaScript |
| CSS animations (no JS) | Smooth effects with no JS overhead |
| Inline SVG favicon | Zero HTTP request for icon |
| Font swap (`media="print"`) | Non-blocking font loading, no FOIT |
| `clamp()` typography | Perfect fluid scaling, zero layout shift |
| `prefers-reduced-motion` | Accessibility compliance |
| JSON-LD schemas | Google-recommended structured data format |

---

*Built with ❤️ by **Aqsa Zam Zam Mirza Johar Baig** — Software Developer & Creator of Alerto*
