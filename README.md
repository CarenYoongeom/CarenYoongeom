# KSMC — AI Sales Agent Platform

> **ABP Capstone Project · SKK GSB · 2026**
> Customer-facing site for a multi-agent semiconductor sales automation system.

[![Live Demo](https://img.shields.io/badge/Live%20Demo-online-2D6A4F?style=flat-square)](https://profound-caramel-e9af16.netlify.app)
[![Status](https://img.shields.io/badge/Status-in%20progress-C9501C?style=flat-square)]()
[![License](https://img.shields.io/badge/License-MIT-0A0F1C?style=flat-square)](./LICENSE)

---

## What This Is

**KSMC** is a fictitious mid-sized fabless semiconductor designer used as the business context for an Agentic Business Platform capstone. The fictional KSMC operates across 5nm–180nm process nodes, serves industrial / automotive / consumer / IoT markets, and handles ~450 SKUs.

The capstone project builds a **multi-agent system** that replaces the manual 24–48 hour B2B inquiry process with an automated sub-4-hour pipeline. This repository currently contains the **customer-facing site** — the entry point where prospective buyers submit technical and commercial inquiries.

## Current Status

This repository is under active development for the ABP final presentation.

| Component | Status | Location |
|-----------|--------|----------|
| Customer-facing site (HTML/CSS/JS) | ✅ Complete | [`index.html`](./index.html) |
| Apps Script backend (form → Sheets) | 🚧 In progress | Not yet committed |
| n8n agent workflow (Sheets → agents → Gmail) | 🚧 In progress | Not yet committed |
| Privacy consent (PIPA + GDPR) | ✅ Complete | Embedded in `index.html` |
| Live deployment | ✅ Online | [Netlify](https://profound-caramel-e9af16.netlify.app) |

The site is fully functional as a standalone form. Form submissions are routed to a sandboxed backend during development.

## The Site

`index.html` is a single-file static site that includes:

- **Hero, Technology, Products, Quality** — KSMC brand presence sections
- **Contact form** — 13-field inquiry form with auto-generated `INQ-MMDDYYYY-XXXX` identifier
- **Privacy consent** — 3-tier PIPA-style consent block (master + 2 required + 1 optional) with modal disclosures referencing both GDPR Article 13 and Korean Personal Information Protection Act
- **Export compliance notice** — pre-flight Guardrail disclosure (EAR / ITAR / BIS Entity List)
- **~450 chip ID autocomplete** — datalist of full KSMC catalogue for the inquiry form

No build step, no framework, no dependencies beyond Google Fonts. Drop into any static host.

## Design Language

The site rejects generic SaaS aesthetics in favor of an editorial, technical-document tone:

- **Type**: IBM Plex Sans (body), IBM Plex Mono (specs and labels), IBM Plex Serif (italic emphasis)
- **Palette**: ink `#0A0F1C`, paper `#F5F3EE`, copper `#C9501C`, line `#D6D1C4`
- **Layout**: 1px borders instead of shadows, flat surfaces, numbered section indices (01, 02, 03, 04)
- **Inspiration**: TSMC's restraint, Samsung Healthcare's clarity, the visual density of an engineering datasheet

The copper accent (`#C9501C`) references the conductive copper traces on a printed circuit board — KSMC's signature color tied to the product itself rather than an arbitrary brand choice.

## Deploy

The site is a single HTML file. To host your own copy:

**Option A — Netlify Drop (no signup required)**
1. Rename `index.html` if needed
2. Drag and drop to https://app.netlify.com/drop
3. URL issued in 30 seconds

**Option B — GitHub Pages (this repository)**
1. Repository Settings → Pages → Source: `main` branch, `/` (root)
2. Wait 2-3 minutes for first deploy
3. Site live at `https://yourname.github.io`

**Option C — Any static host**
Drop `index.html` anywhere that serves HTML — Cloudflare Pages, Vercel, even a USB stick opened in a browser.

## Roadmap

What's coming as the project completes:

- [ ] Commit Google Apps Script source (form → Google Sheets ingest)
- [ ] Commit n8n workflow JSON (Sheets → multi-agent pipeline → Gmail)
- [ ] `docs/architecture.md` — agent role definitions, sequential pipeline pattern
- [ ] `docs/setup-guide.md` — end-to-end deployment for new operators
- [ ] `docs/demo-script.md` — 3-minute live demo flow
- [ ] Repo restructure into personal portfolio with KSMC under `projects/ksmc/`

## Acknowledgments

Built for the **Agentic Business Platform (ABP)** capstone module at **SKK GSB** (Sungkyunkwan University Graduate School of Business), 2026 cohort.

KSMC is a fictional entity used solely for academic purposes. Any resemblance to real Korean semiconductor manufacturers is coincidental.

## License

MIT — see [`LICENSE`](./LICENSE). Code is free to reuse; the KSMC brand identity and fictional business narrative are part of an academic project and not for commercial use.

---

*This repository will transition into a personal portfolio site after the ABP final presentation, with the KSMC project preserved as the inaugural case study.*
