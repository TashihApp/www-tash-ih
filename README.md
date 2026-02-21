# tash.ih

Landing page and privacy policy for [Tashih](https://tash.ih), a native macOS application that enhances Turkish long-form text using local AI. The site serves as the public-facing product page, privacy policy, and App Store marketing link destination.

**Live:** [https://tash.ih](https://tash.ih)

---

## Overview

This repository contains the static website for the Tashih macOS application. The site is built with pure HTML, CSS, and vanilla JavaScript — no build step, no dependencies, no frameworks. It's designed to load instantly and render beautifully on all devices.

---

## Pages

### Landing Page (`index.html`)

The main product page includes:

- **Hero section** — App title, tagline, and call-to-action download button
- **Product overview** — Key value proposition: local AI, privacy-first, Turkish-native
- **Enhancement pipeline** — Visual walkthrough of the text enhancement flow
- **6 Use Cases** — Academic writing, journalism, technical blog, official correspondence, literary essay, translation review
- **Feature highlights** — Multi-format import/export, diff view, feedback loop, session history
- **Pricing** — 14-day free trial with lifetime purchase option
- **Footer** — Links, credits, and legal

**SEO & Social:**
- Open Graph meta tags for rich link previews
- Twitter Card meta tags
- Turkish-language `<html lang="tr">` for search engine localization
- Descriptive meta description and keywords

### Privacy Policy (`privacy.html`)

Comprehensive privacy policy covering:
- On-device processing guarantee (no text leaves the Mac)
- No analytics or telemetry
- No user accounts or cloud sync
- Local-only data storage via SwiftData
- App Store purchase handled entirely by Apple

---

## Design

The site uses a dark theme with an amber accent (`#F5A623`) matching the Tashih app's brand identity.

**Design Tokens:**
| Token | Value |
|---|---|
| Accent | `#F5A623` (amber/golden) |
| Background | `#09090b` (near-black) |
| Card background | `#111113` |
| Text | `#fafafa` (near-white) |
| Secondary text | `#a1a1aa` |
| Border radius | 16px |

**Typography:** SF Pro Display / SF Pro Text / system-ui stack, matching macOS native appearance.

---

## Domain Configuration

| File | Purpose |
|---|---|
| `CNAME` | Custom domain: `tash.ih` |

DNS is managed through Cloudflare with CNAME records pointing to GitHub Pages.

---

## Deployment

The site is hosted on **GitHub Pages** and deployed automatically on push to `main`.

```bash
# Deploy: just push to main
git add . && git commit -m "update" && git push
```

No build step is required. GitHub Pages serves the static files directly.

---

## Local Development

```bash
# Clone the repository
git clone https://github.com/TashihApp/www-tash-ih.git
cd www-tash-ih

# Open in browser (macOS)
open index.html

# Or use a local server for accurate path resolution
python3 -m http.server 8000
# → http://localhost:8000
```

---

## Project Structure

```
www-tash-ih/
├── index.html    # Landing page — product overview, features, pricing
├── privacy.html  # Privacy policy
├── CNAME         # Custom domain configuration (tash.ih)
├── .gitignore    # Standard exclusions
└── README.md     # This file
```

---

## Related Repositories

| Repository | Description |
|---|---|
| [TashihApp](https://github.com/TashihApp) | GitHub organization |
| [tashih-core](https://github.com/TashihApp/tashih-core) | Foundation package — domain models |
| [tashih-muharrir-kit](https://github.com/TashihApp/tashih-muharrir-kit) | LLM integration engine |
| [tashih-feature-enhance](https://github.com/TashihApp/tashih-feature-enhance) | Enhancement pipeline |
| [tashih-feature-ui](https://github.com/TashihApp/tashih-feature-ui) | Design system and components |
| [tashih-feature-import](https://github.com/TashihApp/tashih-feature-import) | Document import (PDF, DOCX, MD, TXT) |
| [tashih-feature-export](https://github.com/TashihApp/tashih-feature-export) | Multi-format export |
| [tashih-feature-storage](https://github.com/TashihApp/tashih-feature-storage) | SwiftData persistence |
| [tashih-feature-store](https://github.com/TashihApp/tashih-feature-store) | StoreKit 2 monetization |

---

## License

This website is part of the [Tashih](https://tash.ih) project. All rights reserved.
