# CLAUDE.md

## Project Overview

**npfdemo** is a Not-For-Profit sector demo web application for Simpson Associates (Data Transformation Consultancy). It showcases interactive data analytics dashboards for the charity/NFP sector, covering three verticals: Fundraising, Partnerships, and Operations.

## Repository Structure

```
npfdemo/
├── CLAUDE.md                        # AI assistant guide (this file)
├── SPECIFICATION.md                 # Full application specification
├── README.md                        # Project readme
├── TSI GTM.pdf                      # Go-To-Market strategy document
├── Police Hotspot Landing Page.html # Design reference (separate sector)
└── index.html                       # The NFP demo application (single-file)
```

## Technology Stack

- **Single HTML file** — no build tools, no server, no dependencies to install
- **Chart.js 4.4.1** — via CDN for all chart visualizations
- **Leaflet 1.9.4** — via CDN for the service coverage map
- **JetBrains Mono** — via Google Fonts for monospace values
- **Silka** — custom font from simpson-associates.co.uk
- **CARTO Light** — tile layer for the Leaflet map
- All synthetic data is embedded inline in JavaScript

## Development Setup

No build system or package manager needed. Simply open `index.html` in a browser.

## Common Commands

```bash
# Open the app in a browser (Linux)
xdg-open index.html

# Serve locally (optional, if CORS issues arise with fonts)
python3 -m http.server 8000
```

## Architecture

The application is a single self-contained HTML file following the Police Hotspot Landing Page design patterns:

- **CSS**: All styles inline in `<style>` block, using CSS variables for the Simpson Associates design system
- **HTML**: 4 top-level pages (Dashboard, Solutions, Case Studies, Contact), 6 dashboard panels
- **JavaScript**: All logic inline in `<script>` block at end of body
- **Navigation**: Client-side page switching via `showPage()` and dashboard tab navigation via data-panel attributes
- **Charts**: 16+ Chart.js instances for data visualization
- **Map**: Leaflet map with circle markers for 34 service delivery locations
- **Data**: Synthetic data for fictional "Hope & Compass" charity embedded in JS

### Dashboard Panels
1. **Executive Summary** — KPIs, income trends, source mix, impact, radar
2. **Fundraising & Engagement** — donation trends, segmentation, campaigns, channels, retention, LTV
3. **Partnership Intelligence** — health distribution, type breakdown, scoring radar, activity, rankings table
4. **Operations & Volunteers** — demand forecasting, volunteer hours, resource utilisation, outcomes, Leaflet map
5. **Benchmarks & Comparison** — KPI benchmark bars, data maturity radar, scatter plot, income diversification
6. **AI Insights** — filterable AI-generated insight cards by vertical and priority

## Guidelines for AI Assistants

- Read this file at the start of every session to understand current project state.
- Keep this file updated as the project evolves.
- Prefer editing existing files over creating new ones.
- Do not over-engineer; keep changes minimal and focused on the task at hand.
- Write clear, descriptive commit messages.
- The design reference is `Police Hotspot Landing Page.html` — follow its CSS patterns and naming conventions.
- The full specification is in `SPECIFICATION.md` — refer to it for detailed requirements.
