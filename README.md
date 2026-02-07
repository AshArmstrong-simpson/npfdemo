# NFP Demo — Simpson Associates

Interactive data analytics demo for the Not-For-Profit sector, built by [Simpson Associates](https://www.simpson-associates.co.uk/).

## What is this?

A single-file HTML application showcasing data transformation capabilities across three charity verticals — **Fundraising**, **Partnerships**, and **Operations** — using synthetic data for the fictional charity **Hope & Compass**.

Built to mirror the design and architecture of the Police Hotspot Landing Page, this demo serves as a sales enablement tool for the Simpson Associates BD team.

## Features

- **6 interactive dashboard panels** with 16+ Chart.js visualisations and a Leaflet map
- **Lazy-loaded charts** initialised on first panel view for performance
- **Functional filters and toggles** that update charts in real-time
- **Sortable data tables** for partnership rankings and donor segments
- **AI Insights panel** with 9 ML-generated recommendations across all verticals
- **Real case studies** from Simpson Associates clients (BHF, Alzheimer's Society, Commissioning Alliance, Flagship Group)
- **Responsive design** at 1100px and 700px breakpoints
- **UK market aligned** — British spellings, GBP, SORP, NCVO, Data Orchard frameworks

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Application | Single self-contained HTML file |
| Charts | Chart.js 4.4.1 (CDN) |
| Map | Leaflet 1.9.4 (CDN) |
| Fonts | Silka (Simpson Associates), JetBrains Mono (Google Fonts) |
| Map tiles | CARTO Light |
| Data | Synthetic, embedded inline in JavaScript |

No build tools, no server, no dependencies. Just open `index.html` in a browser.

## Quick Start

```bash
# Option 1: Open directly
open index.html

# Option 2: Serve locally (if font CORS issues arise)
python3 -m http.server 8000
```

## Documentation

- **[SPECIFICATION.md](SPECIFICATION.md)** — Full application specification (v1.1)
- **[CLAUDE.md](CLAUDE.md)** — AI assistant guide and architecture reference
- **[TSI GTM.pdf](TSI%20GTM.pdf)** — Go-To-Market strategy document

## Design Reference

The application follows the exact design system from `Police Hotspot Landing Page.html` — same CSS variables, component patterns, typography, and colour palette.
