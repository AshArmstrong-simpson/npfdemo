# NFP Demo Application — Detailed Specification

**Project:** Simpson Associates Not-For-Profit Sector Demo
**Version:** 1.1
**Date:** 7 February 2026
**Author:** Simpson Associates Data Transformation Consultancy
**Status:** Implemented

---

## Table of Contents

1. [Executive Summary](#1-executive-summary)
2. [Business Context & Objectives](#2-business-context--objectives)
3. [Research Findings](#3-research-findings)
   - 3.1 [Sector Landscape](#31-sector-landscape)
   - 3.2 [Competitor Analysis](#32-competitor-analysis)
   - 3.3 [Microsoft Nonprofit Offerings](#33-microsoft-nonprofit-offerings)
   - 3.4 [Key Sector KPIs & Benchmarks](#34-key-sector-kpis--benchmarks)
4. [Application Architecture](#4-application-architecture)
   - 4.1 [Technology Stack](#41-technology-stack)
   - 4.2 [Design System](#42-design-system)
   - 4.3 [Page Structure](#43-page-structure)
5. [Synthetic Data Model](#5-synthetic-data-model)
   - 5.1 [Fictional Organisation](#51-fictional-organisation)
   - 5.2 [Fundraising Data](#52-fundraising-data)
   - 5.3 [Partnership Data](#53-partnership-data)
   - 5.4 [Operations Data](#54-operations-data)
6. [Page-by-Page Specification](#6-page-by-page-specification)
   - 6.1 [Dashboard Page — Executive Summary](#61-dashboard-page--executive-summary)
   - 6.2 [Dashboard Page — Fundraising & Engagement](#62-dashboard-page--fundraising--engagement)
   - 6.3 [Dashboard Page — Partnership Intelligence](#63-dashboard-page--partnership-intelligence)
   - 6.4 [Dashboard Page — Operations & Volunteers](#64-dashboard-page--operations--volunteers)
   - 6.5 [Dashboard Page — Benchmarks & Comparison](#65-dashboard-page--benchmarks--comparison)
   - 6.6 [Dashboard Page — AI Insights](#66-dashboard-page--ai-insights)
   - 6.7 [Solutions Page](#67-solutions-page)
   - 6.8 [Case Studies Page](#68-case-studies-page)
   - 6.9 [Contact Page](#69-contact-page)
7. [Interaction Patterns](#7-interaction-patterns)
8. [Responsive Design](#8-responsive-design)
9. [Alignment to TSI GTM Strategy](#9-alignment-to-tsi-gtm-strategy)
10. [Microsoft Technology Alignment](#10-microsoft-technology-alignment)
11. [Implementation Phases](#11-implementation-phases)
12. [Appendices](#appendices)

---

## 1. Executive Summary

This document specifies a comprehensive single-page web application that demonstrates Simpson Associates' data transformation capabilities for the Not-For-Profit (NFP) sector. The application serves as a live, interactive demo — equivalent to the existing Police Hotspot Landing Page built for the policing sector — showcasing breadth of service across three core verticals: **Fundraising**, **Partnerships**, and **Operations**.

The demo uses entirely synthetic data for a fictional UK charity and is built as a standalone HTML file with no server dependencies, suitable for hosting on GitHub Pages, Azure Static Web Apps, or embedding in sales presentations.

**Key differentiators over competitor demos:**
- Interactive dashboards with real-time chart manipulation (not static screenshots)
- Coverage of all three TSI GTM verticals in a single unified experience
- Sector-specific KPIs grounded in real UK charity benchmarks
- Clear alignment to Microsoft's nonprofit technology stack (Fabric, Power BI, Azure, CDM)
- Evidence of AI/ML capabilities (segmentation models, demand forecasting, partnership scoring)

---

## 2. Business Context & Objectives

### 2.1 About Simpson Associates

Simpson Associates is a York-based data transformation consultancy and Microsoft Partner of the Year. The firm holds ISO 27001, ISO 9001, and Cyber Essentials Plus accreditations. Their offices are in York and Sheffield.

### 2.2 Strategic Context

The TSI (Third Sector Industry) Go-To-Market strategy document outlines a repeatable framework across three verticals:

| Focus | Revenue | Reach | Cost |
|-------|---------|-------|------|
| **Vertical** | **Fundraising** | **Partnerships** | **Operations** |
| Connect | Donor Data Integration | Partnership Data Centralisation | Volunteer Data Integration |
| Analyse | Donor Segmentation & Personalisation Model | Partnership Scoring Model | Service Demand Forecasting Model |
| Consume | Fundraising & Engagement Dashboard | Partnership Monitoring Dashboard | Operational Management Dashboard |

Each vertical is underpinned by:
- Data Strategy & Operating Model
- AI Readiness & Analytic Maturity
- Cloud Infrastructure Foundations
- Management & Governance Principles
- Advanced Analytics & AI Capabilities
- Training, Enablement & Knowledge Share

### 2.3 Objectives for the Demo Application

1. **Demonstrate breadth** — show capabilities across all three verticals, not just one
2. **Interactive evidence** — provide working charts, filters, and drill-downs, not static images
3. **Sector credibility** — use realistic KPIs, benchmarks, and terminology from the UK charity sector
4. **Technology showcase** — reference Microsoft stack alignment (Azure, Fabric, Power BI, CDM)
5. **Sales enablement** — give the BD team a tangible artefact for meetings and pitches
6. **Competitive differentiation** — go beyond what Blackbaud, Salesforce, and specialist consultancies offer in their demo experiences

---

## 3. Research Findings

### 3.1 Sector Landscape

The UK charity sector comprises approximately 170,000 registered charities. Key structural characteristics:

**Regulatory environment:**
- Charities SORP 2026 (effective 1 January 2026) introduces a new three-tier reporting framework:
  - Tier 1: Income up to £500,000
  - Tier 2: Income £500k–£15m
  - Tier 3: Income above £15m
- Charity Commission for England & Wales, OSCR (Scotland), CCNI (Northern Ireland)
- GDPR and the Data Protection Act 2018 apply with heightened public expectation

**Data maturity:**
- Only 1 in 4 charities say data is a priority (Charity Digital Skills Report 2024)
- 46% of NFPs rate themselves at the middle "Learning" stage of data maturity (Data Orchard)
- 30% of UK charities have no CRM at all — relying on spreadsheets (Teque)
- 4 in 10 lack time to focus on data; 26% feel they are not making the most of their CRM

**Key data challenges:**
1. Low data prioritisation and investment
2. Poor data quality (worst sector for contacting deceased individuals)
3. Resource constraints limiting analytics investment
4. Fragmented systems with low CRM adoption
5. Regulatory complexity (GDPR, data governance)
6. Impact measurement difficulty (outputs vs. outcomes vs. long-term impact)

### 3.2 Competitor Analysis

#### Tier 1: Specialist NFP Data Analytics (UK)

| Competitor | Offering | Demo Format |
|-----------|----------|-------------|
| **Wood for Trees** (Salocin Group) | Predictive donor modelling, segmentation, fundraising optimisation | Whitepapers, case studies |
| **THINK Consulting Solutions** | Fundraising strategy, individual giving programme review | Published reports, strategy content |
| **Teque** | Bespoke CRM, donor management, volunteer portals | Free Charity Health Check benchmarking tool |
| **Data Orchard CIC** | Data Maturity Framework (7 themes, 5 stages) | Free online self-assessment tool |
| **Infoboss** | Automated data management (Elastic Stack) | Platform demo |

#### Tier 2: Major Platforms

| Competitor | Offering | Demo Format |
|-----------|----------|-------------|
| **Blackbaud** | Raiser's Edge NXT, eTapestry, "Intelligence for Good" AI | Scheduled live demos, AI announcements |
| **Salesforce Nonprofit Cloud** | CRM, Einstein AI, Tableau Accelerators | Pre-built Tableau dashboards, live demos |
| **Donorfy / Access Group** | UK NFP CRM with built-in analytics | Bookable live demos, downloadable brochures |
| **Sage Intacct** | Financial management, 200+ prebuilt visualisations | Dashboard examples in documentation |

#### Tier 3: Large Consultancies with NFP Practice

KPMG, Deloitte, Sopra Steria, FTI Consulting — advisory-led, no interactive demos.

#### Market Gap Identified

No competitor offers a **single interactive demo** that spans fundraising analytics, partnership intelligence, AND operational efficiency in one unified experience. Most offer either:
- Benchmarking tools (one dimension only)
- Static case studies / whitepapers
- Live demos requiring scheduling and sales engagement

This gap is the core opportunity for the Simpson Associates demo.

### 3.3 Microsoft Nonprofit Offerings

Simpson Associates is a Microsoft Partner. The demo must clearly reference and align to Microsoft's nonprofit technology stack:

#### Common Data Model (CDM) for Nonprofits
- Open-source data schema with 90+ entity definitions
- Covers: Constituent Management, Fundraising, Awards, Program Delivery, Impact Tracking
- Key entities: DonorCommitment, DesignatedCredit, Disbursement, DeliveryFramework, Indicator, BenefitRecipient
- Available on GitHub and AppSource

#### Power Platform Solutions
| Solution | Type | Purpose |
|----------|------|---------|
| Fundraising | Model-driven Power App | Donor management, gift tracking, campaign management |
| Grant Management | Model-driven Power App | End-to-end grant cycle (request → award → reporting → disbursement) |
| Volunteer Management | Model-driven Power App | Staff-facing volunteer lifecycle management |
| Volunteer Engagement | Power Pages portal | Self-service volunteer discovery and application |
| Outcome Management | Model-driven Power App | Programme outcomes and impact insights |

#### Power BI Dashboards
| Dashboard | Purpose |
|-----------|---------|
| Fundraising Performance Dashboard | Donors, fundraising, campaign outcomes in near-real-time |
| Program Impact Dashboard | Interrelates fundraising and programme data for impact reporting |

#### Microsoft Fabric — Nonprofit Data Solutions (Preview)
- Medallion lakehouse architecture (Bronze → Silver → Gold)
- Pre-built pipelines, notebooks (PySpark), semantic models, Power BI reports
- Supports Dynamics 365 + CDM and Salesforce NPSP as data sources
- Outputs: fundraising intelligence, constituent analytics, engagement dashboards

#### Azure Landing Zone for Nonprofits
- Preconfigured cloud blueprint for secure, scalable setup
- Core: Networking, Management, Identity, Security

#### Microsoft 365 Templates
- Volunteer Center (SharePoint)
- Manage Volunteers (Teams)

### 3.4 Key Sector KPIs & Benchmarks

These benchmarks are drawn from published UK sector studies (AAW Group, M+R/Rally, CAF UK Giving Report, NCVO Almanac, Teque, Charity Accounting Partners) and inform the synthetic data in the demo.

#### Fundraising KPIs

| Metric | Description | UK Benchmark |
|--------|-------------|--------------|
| Donor Retention Rate | % of donors who give again year-on-year | 40% average (60% attrition); first-time 20%; repeat 60%+ |
| Average Gift Size | Mean donation value | £72/month among active donors; £260 annual |
| Donor Lifetime Value (LTV) | Total projected giving over the relationship | £780 (3-year average) |
| Cost per £ Raised | Fundraising cost / total raised | 25p per £1 (4:1 return); 10–25% highly efficient |
| Fundraising ROI | Return per £ invested | £4 returned per £1 spent (NCVO Almanac) |
| LTV:CAC Ratio | Lifetime value vs. cost of acquisition | Target >3:1 |
| Recurring vs. One-time | Split of regular vs. single gifts | Regular giving revenue growing (+8%); cash declining (−6%) |
| Email Revenue Share | Income attributable to email campaigns | 8% of UK online income |
| Income Diversification | Mix of individuals, corporates, trusts, legacies | Legacies + individual giving = two-thirds for large charities |

#### Partnership KPIs

| Metric | Description |
|--------|-------------|
| Partnership Health Score | Composite of funding success, project completion, strategic alignment, engagement frequency |
| Corporate Income | Tracked as diversification KPI; only 1 in 4 businesses beyond FTSE 100 support charities |
| SROI (Social Return on Investment) | Monetary value assigned to social outcomes per £ invested |
| National TOMs Compliance | Standardised social value measurement; volunteer time valued at £16.50/hr (2026 rate) |
| Joint Initiative Completion Rate | % of co-developed projects delivered to plan |
| Partner Retention Rate | Year-on-year continuation of partnership agreements |

Note: Partnership health scoring is not widely standardised in the UK sector — this is a **differentiation opportunity** for Simpson Associates.

#### Operational KPIs

| Metric | Description |
|--------|-------------|
| Volunteer Retention Rate | Returning volunteers / total previous volunteers × 100 |
| Volunteer Hours & Utilisation | Depth of involvement; tracked with satisfaction surveys |
| Cost per Beneficiary | Total programme cost / unique beneficiaries served |
| Programme Success Rate | % of programme objectives completed |
| Beneficiaries Served | Direct impact measure (with deduplication) |
| Fund Utilisation Ratio | % of budget directly supporting programmes vs. overhead |
| Overhead Ratio | Admin + fundraising costs / total expenditure; sector average 69% charitable activities |
| Months of Operating Reserves | Cash on hand / average monthly expenditure |

---

## 4. Application Architecture

### 4.1 Technology Stack

The application is a **single self-contained HTML file** with all CSS and JavaScript inline. This mirrors the architecture of the Police Hotspot Landing Page and enables:
- Zero build step — open directly in a browser
- Easy sharing via email, USB, or any static hosting
- No server-side dependencies
- Offline capability for in-person demos

**Client-side libraries (loaded via CDN):**

| Library | Version | Purpose |
|---------|---------|---------|
| Chart.js | 4.4.1 | All chart visualisations (line, bar, doughnut, radar, scatter, pie) |
| Leaflet | 1.9.4 | Geographic map for service delivery coverage (Operations tab) |
| Google Fonts | — | JetBrains Mono (monospace data values) |

**Custom fonts (loaded from simpson-associates.co.uk):**

| Font | Weights | Usage |
|------|---------|-------|
| Silka | 400, 500, 600, 700 | All body text, headings, labels |
| JetBrains Mono | 500, 600 | KPI values, data figures, table cells |

**Map tiles:** CARTO Light (via `basemaps.cartocdn.com`)

### 4.2 Design System

The design system is inherited directly from the Police Hotspot Landing Page to ensure brand consistency across Simpson Associates demos.

#### Colour Palette

| Token | Hex | Usage |
|-------|-----|-------|
| `--navy` | `#2A4149` | Header, hero, dark backgrounds |
| `--navy-2` | `#22353C` | Secondary dark backgrounds |
| `--navy-3` | `#2E4A53` | Tertiary dark backgrounds |
| `--blue` | `#2C83D3` | Primary accent, active states, links |
| `--blue-d` | `#226A92` | Hover states for primary accent |
| `--blue-l` | `#5BA8E6` | Light accent variant |
| `--teal` | `#10CA72` | Success, positive trends, green indicators |
| `--teal-l` | `#3DD98D` | Hero stat values, light green |
| `--purple` | `#8876E4` | Tertiary accent, partnership vertical |
| `--red` | `#EF4444` | Critical alerts, negative trends |
| `--orange` | `#F97316` | Warning states, high priority |
| `--amber` | `#EAB308` | Caution, medium priority |
| `--green` | `#10CA72` | Good status, low risk |
| `--sa-gradient` | `linear-gradient(-37deg, #8876E4 0%, #1E8BC8 98%)` | Brand gradient for hero and feature cards |

#### Grey Scale

| Token | Hex | Usage |
|-------|-----|-------|
| `--g50` | `#F3F1ED` | Page background |
| `--g100` | `#EBE9E4` | Card hover, subtle borders |
| `--g200` | `#E5E5E5` | Borders, dividers |
| `--g300` | `#CBD5E1` | Input borders, toggle unchecked |
| `--g400` | `#979797` | Muted text, labels |
| `--g500` | `#64748B` | Secondary text |
| `--g600` | `#475569` | Body text |
| `--g700` | `#334155` | Emphasis text |
| `--g800` | `#22353C` | Strong text |
| `--g900` | `#2A4149` | Primary text |

#### Typography

| Element | Font | Size | Weight |
|---------|------|------|--------|
| Page title (h1) | Silka | 3.2rem | 800 |
| Section title (h3) | Silka | 1.05rem | 700 |
| Card title | Silka | 1rem | 600 |
| Body text | Silka | 0.88rem | 400 |
| KPI value | JetBrains Mono | 1.75rem | 700 |
| Table data | JetBrains Mono | 0.9rem | 600 |
| Badge | Silka | 0.72rem | 600 |
| Small label | Silka | 0.75rem | 500 |

#### Spacing & Layout

| Token | Value | Usage |
|-------|-------|-------|
| `--radius` | 10px | Standard border radius for cards |
| `--shadow` | `0 1px 3px rgba(42,65,73,.06), 0 4px 12px rgba(42,65,73,.05)` | Default card shadow |
| `--shadow-lg` | `0 8px 30px rgba(42,65,73,.1)` | Elevated elements (hover, modals) |
| Max width | 1440px | Content container |
| Grid system | 12-column CSS Grid | Layout grid with `span3` through `span12` classes |

#### Component Patterns

| Component | CSS Class | Description |
|-----------|-----------|-------------|
| Header | `.header` | Fixed top bar with logo, nav tabs, demo tag |
| Top Navigation | `.top-nav`, `.top-tab` | Pill-style page switcher in header (scrollable on mobile) |
| Demo Tag | `.demo-tag` | Gradient pill badge "NFP Demo" (hidden on mobile) |
| Hero Section | `.pg-hero` | Full-width dark hero with stats and featured chart |
| Hero Stat | `.hero-stat` | Small stat box inside hero (teal monospace value + label) |
| Dashboard Nav | `.dash-nav`, `.d-tab` | Secondary tab bar for dashboard sub-panels |
| Panel | `.panel` | Content area toggled by dashboard tabs |
| KPI Card | `.kpi` | White card with coloured left border, monospace value, trend indicator |
| Chart Card | `.card`, `.chart-box` | White card containing a Chart.js canvas (280px default height) |
| Filter Bar | `.filters`, `.fsel` | Row of dropdown selects with custom chevron |
| Toggle Switch | `.toggle-wrap`, `.toggle`, `.toggle.on` | Div-based toggle (44×24px, circle slides right when active, blue background) |
| Badge | `.badge`, `.b-info`/`.b-ok`/`.b-warn`/`.b-err` | Coloured pill labels |
| Data Table | `.data-table` | Scrollable sortable data table with sticky header |
| Insight Card | `.ins` | Dark-background card with priority badge and description |
| Solution Card | `.sol-card` | White card with icon, title, description, stats row |
| Case Study Card | `.cs-card` | Card with gradient header, body, metrics, tag |
| Contact Form | `.c-form` | Standard form with label, input, textarea, button |

### 4.3 Page Structure

The application has four top-level pages, with the Dashboard page containing six sub-panels:

```
Header [Logo] [Dashboard | Solutions | Case Studies | Contact] [NFP Demo]

├── Dashboard Page
│   ├── Hero Section (title, subtitle mentioning Hope & Compass, summary stats, featured doughnut)
│   ├── Dashboard Nav Tabs
│   │   ├── Executive Summary    ← Overview KPIs across all verticals
│   │   ├── Fundraising          ← Donor analytics, segmentation, campaigns
│   │   ├── Partnerships         ← Scoring, health monitoring, collaboration
│   │   ├── Operations           ← Volunteers, service demand, resources
│   │   ├── Benchmarks           ← Sector comparison, data maturity
│   │   └── AI Insights          ← AI-generated recommendations
│   └── Main Content Area
│
├── Solutions Page
│   ├── Page Hero
│   └── Solution Cards Grid (6 cards)
│
├── Case Studies Page
│   ├── Page Hero
│   └── Case Study Cards Grid (4 real Simpson Associates clients)
│
├── Contact Page
│   ├── Page Hero
│   └── Two-column: Form + Info Cards
│
└── Footer
```

---

## 5. Synthetic Data Model

### 5.1 Fictional Organisation

**Name:** Hope & Compass Foundation
**Type:** Registered UK charity (Tier 2 under SORP 2026)
**Charity Number:** 1187452 (fictional)
**Headquarters:** Leeds, West Yorkshire
**Regional offices:** Manchester, Newcastle, Sheffield
**Founded:** 2009
**Mission:** Supporting vulnerable communities across Northern England through homelessness prevention, youth development, and community wellbeing programmes.

**Annual profile:**

| Metric | Value |
|--------|-------|
| Total annual income | £12.4M |
| Voluntary income | £8.6M |
| Grant income | £2.8M |
| Trading/earned income | £1.0M |
| Total expenditure | £11.1M |
| Charitable activities spend | £7.9M (71%) |
| Fundraising costs | £1.8M (16%) |
| Support/governance costs | £1.4M (13%) |
| Employees (FTE) | 186 |
| Active volunteers | 1,247 |
| Beneficiaries served annually | 28,450 |
| Service delivery locations | 34 across Northern England |

**Programme areas:**
1. **Safe Homes** — Homelessness prevention, emergency accommodation, tenancy support
2. **Future Foundations** — Youth mentoring, skills training, employability programmes
3. **Community Wellbeing** — Mental health support, food banks, social inclusion activities

### 5.2 Fundraising Data

#### Donor Base Summary

| Segment | Count | Avg Annual Gift | Retention Rate | LTV (3yr) |
|---------|-------|----------------|----------------|-----------|
| Major Donors (£5,000+) | 42 | £12,400 | 88% | £34,100 |
| Mid-Level (£1,000–£4,999) | 318 | £2,150 | 72% | £5,400 |
| Regular Givers (monthly) | 3,840 | £384/yr (£32/mo) | 68% | £1,020 |
| One-time Donors | 8,920 | £45 | 22% | £58 |
| Lapsed (12mo+ no gift) | 4,150 | — | Re-activation target: 8% | — |
| **Total active donors** | **13,120** | | | |

#### Campaign Data (12 months)

| Campaign | Channel | Income | Donors | Conversion | Cost | ROI |
|----------|---------|--------|--------|------------|------|-----|
| Winter Appeal 2025 | Direct mail + email | £1,240,000 | 4,200 | 8.2% | £148,000 | 8.4:1 |
| Spring Gala | Event | £420,000 | 180 | 62% | £95,000 | 4.4:1 |
| Big Give Christmas | Online | £680,000 | 2,100 | 12.4% | £42,000 | 16.2:1 |
| Emergency Housing Appeal | Email + social | £310,000 | 1,850 | 6.8% | £28,000 | 11.1:1 |
| Youth Futures Campaign | Social media | £185,000 | 3,200 | 3.2% | £62,000 | 3.0:1 |
| Legacy Giving Programme | Direct mail | £890,000 | 28 new pledges | — | £45,000 | 19.8:1 |
| Corporate Partnerships | Relationship | £1,420,000 | 47 partners | — | £180,000 | 7.9:1 |
| Regular Giving Acquisition | F2F + digital | £460,000 | 960 new | 4.1% | £232,000 | 2.0:1 |

### 5.3 Partnership Data

#### Active Partnerships (47 total)

| Partner | Type | Annual Value | Health Score | Status |
|---------|------|-------------|-------------|--------|
| Yorkshire Building Society | Corporate Sponsor | £280,000 | 94 | Platinum |
| Northern Powerhouse Trust | Grant Funder | £420,000 | 91 | Platinum |
| Leeds City Council | Statutory | £380,000 | 87 | Gold |
| ASDA Foundation | Corporate Sponsor | £165,000 | 85 | Gold |
| The National Lottery Community Fund | Grant Funder | £520,000 | 92 | Platinum |
| University of Leeds | Academic | £85,000 | 78 | Silver |
| Greggs Foundation | Corporate Sponsor | £120,000 | 82 | Gold |
| NHS Leeds CCG | Statutory | £240,000 | 76 | Silver |
| Sheffield City Region | Statutory | £195,000 | 80 | Gold |
| Garfield Weston Foundation | Trust/Foundation | £150,000 | 89 | Gold |

*(Plus 37 additional partners in the synthetic dataset at Bronze/Silver/Gold tiers)*

#### Partnership Health Score Components

The scoring model uses four weighted dimensions:

| Dimension | Weight | Description |
|-----------|--------|-------------|
| Funding Reliability | 30% | Consistency of funding commitments, payment timeliness |
| Project Success | 25% | Joint initiative completion rate, outcome achievement |
| Strategic Alignment | 25% | Mission fit, shared values, complementary capabilities |
| Engagement Frequency | 20% | Meeting cadence, communication responsiveness, event participation |

**Score bands:**
- 90–100: Platinum (strategic priority, deepen relationship)
- 75–89: Gold (healthy, maintain and grow)
- 60–74: Silver (adequate, identify improvement areas)
- Below 60: Bronze (at-risk, intervention needed)

### 5.4 Operations Data

#### Volunteer Workforce

| Metric | Value |
|--------|-------|
| Active volunteers | 1,247 |
| New volunteers (this year) | 312 |
| Volunteer retention rate | 71% |
| Total volunteer hours (annual) | 142,000 |
| Average hours per volunteer/month | 9.5 |
| Volunteer satisfaction score | 8.4/10 |

#### Service Demand Data (Monthly)

| Month | Beneficiaries | Service Sessions | Capacity Used |
|-------|--------------|-----------------|---------------|
| Feb 2025 | 2,180 | 4,850 | 78% |
| Mar 2025 | 2,240 | 5,020 | 80% |
| Apr 2025 | 2,100 | 4,680 | 75% |
| May 2025 | 2,050 | 4,520 | 72% |
| Jun 2025 | 1,980 | 4,380 | 70% |
| Jul 2025 | 1,920 | 4,240 | 68% |
| Aug 2025 | 1,890 | 4,180 | 67% |
| Sep 2025 | 2,280 | 5,100 | 82% |
| Oct 2025 | 2,450 | 5,480 | 88% |
| Nov 2025 | 2,680 | 5,960 | 95% |
| Dec 2025 | 2,840 | 6,280 | 100% |
| Jan 2026 | 2,720 | 6,040 | 97% |

#### Beneficiary Outcomes (Annual)

| Outcome | Target | Actual | Achievement |
|---------|--------|--------|-------------|
| Individuals housed (Safe Homes) | 850 | 812 | 96% |
| Young people completing programmes | 1,200 | 1,084 | 90% |
| Employment outcomes | 420 | 388 | 92% |
| Mental health assessments completed | 2,400 | 2,256 | 94% |
| Food bank visits served | 18,000 | 19,240 | 107% |
| Community events delivered | 240 | 228 | 95% |

---

## 6. Page-by-Page Specification

### 6.1 Dashboard Page — Executive Summary

**Purpose:** Provide a high-level overview across all three verticals, enabling stakeholders to see organisational health at a glance.

**Hero Section:**
- **Title:** "Not-For-Profit Data Analytics & AI" with gradient text on "Data Analytics & AI"
- **Subtitle:** "Data-driven insights for fundraising optimisation, partnership intelligence, and operational excellence — built on Microsoft Azure & Fabric for charities and social enterprises. This demo uses synthetic data for the fictional charity Hope & Compass to showcase our solutions."
- **Hero stats** (4 boxes):
  - £12.4M Total Income
  - 62% Donor Retention
  - 47 Active Partnerships
  - 28,450 Beneficiaries Served
- **Hero visualisation** (right column): Income breakdown doughnut chart (Individual Giving, Grants & Trusts, Corporate, Events, Trading) with a "Synthetic demo data" live indicator

**KPI Row (5 cards):**

| KPI | Value | Colour | Trend |
|-----|-------|--------|-------|
| Total Donations (YTD) | £8.24M | Blue | ▲ 8.2% vs prior year |
| Active Donors | 13,120 | Teal | ▲ 4.6% vs prior year |
| Partnership Funding | £5.25M | Purple | ▲ 12.1% vs prior year |
| Volunteer Hours | 142,000 | Amber | ▲ 6.8% vs prior year |
| Cost per Beneficiary | £390 | Green | ▼ 3.2% (improving) |

**Charts (2×2 grid):**

| Chart | Type | Span | Description |
|-------|------|------|-------------|
| Income Trends (12 Months) | Line chart (multi-series) | span7 | Monthly income split by Donations, Grants, Earned income |
| Income Source Mix | Doughnut chart | span5 | Individual, Corporate, Trusts, Statutory, Legacy, Earned |
| Programme Impact | Horizontal bar chart (`indexAxis:'y'`) | span5 | Beneficiary outcomes by programme vs target |
| Financial Health | Radar chart | span7 | 6 dimensions: Income Growth, Donor Retention, Fundraising Efficiency, Data Maturity, Impact Delivery, Financial Resilience |

**Chart defaults (applied globally):**
- Legend position: bottom
- Legend labels: `usePointStyle:true`, `pointStyle:'circle'`, `padding:12`
- Point style: circle (all charts)
- Font: Silka, 11px, colour `#64748B`

### 6.2 Dashboard Page — Fundraising & Engagement

**Purpose:** Deep-dive into donor analytics, segmentation, and campaign performance — demonstrating the Fundraising Analytics Platform from the GTM document.

**Filters:**
- Time period: Last 3 months / 6 months / 12 months / All time
- Campaign: All / Winter Appeal / Spring Gala / Big Give / etc.
- Toggle: "Show segments" (switches segmentation doughnut between count and value view)

**KPI Row (5 cards):**

| KPI | Value | Colour | Trend |
|-----|-------|--------|-------|
| Total Donations | £8.24M | Blue | ▲ 8.2% |
| Average Gift | £48.60 | Teal | ▲ 3.1% |
| Donor Retention Rate | 62% | Green | ▲ 2.4pp |
| Cost per £ Raised | £0.22 | Purple | ▼ 4.1% (improving) |
| Online Revenue % | 45% | Amber | ▲ 6.2pp |

**Charts:**

| Chart | Type | Span | Data |
|-------|------|------|------|
| Monthly Donation Trend | Line chart with area fill | span7 | 12-month donations with prior year comparison line |
| Donor Segmentation | Doughnut chart | span5 | Major / Mid-level / Regular / One-time / Lapsed segments by count (toggle to value) |
| Campaign Performance | Grouped bar chart | span8 | Income and cost per campaign |
| Donation Channel Mix | Pie chart | span4 | Online, Direct Mail, Events, Major Gifts, Phone |
| Donor Retention Cohort | Stacked area chart | span6 | 3 cohorts (2021, 2022, 2023) showing retention over 5 years |
| Donor Lifetime Value by Segment | Horizontal bar chart (`indexAxis:'y'`) | span6 | Average 3-year LTV per segment |

**Additional elements:**
- **Donor segment table** below charts: Sortable table showing each segment with count, avg gift, retention rate, LTV, growth trend
- **AI insight callout**: Highlighted box recommending re-activation campaign for lapsed donors with predicted recovery rate

### 6.3 Dashboard Page — Partnership Intelligence

**Purpose:** Demonstrate the Partnership Intelligence Suite — scoring, health monitoring, and collaboration tracking.

**Filters:**
- Partnership type: All / Corporate / Grant Funder / Statutory / Trust / Academic / Community
- Health band: All / Platinum / Gold / Silver / Bronze

**KPI Row (5 cards):**

| KPI | Value | Colour | Trend |
|-----|-------|--------|-------|
| Active Partnerships | 47 | Blue | ▲ 5 new this year |
| Total Partner Funding | £5.25M | Teal | ▲ 12.1% |
| Avg Health Score | 79.4 | Green | ▲ 2.8 points |
| Project Completion Rate | 91% | Purple | ▲ 3.2pp |
| At-Risk Partners | 4 | Red | ▼ 2 fewer (improving) |

**Charts:**

| Chart | Type | Span | Data |
|-------|------|------|------|
| Partnership Health Distribution | Bar chart | span7 | Count of partners in each health band (Platinum/Gold/Silver/Bronze) |
| Funding by Partner Type | Doughnut chart | span5 | Breakdown by Corporate/Grant/Statutory/Trust/Academic/Community |
| Funding Trend (12 Months) | Line chart (multi-series) | span7 | Monthly funding by Corporate, Grants, Statutory |
| Partnership Scoring Radar | Radar chart | span5 | Overlay of top 3 partners across 4 scoring dimensions |
| Collaboration Activity | Stacked bar chart | span12 | Monthly count of meetings and communications |

**Additional elements:**
- **Partnership ranking table**: Sortable by health score, funding, type — showing name, type, annual value, health score, trend, status badge
- **At-risk alert panel**: Highlighted cards for at-risk partnerships with recommended actions

### 6.4 Dashboard Page — Operations & Volunteers

**Purpose:** Demonstrate the Operational Efficiency Platform — volunteer management, service demand forecasting, and resource allocation.

**Filters:**
- Programme: All / Safe Homes / Future Foundations / Community Wellbeing
- Region: All / Leeds / Manchester / Newcastle / Sheffield

**Note:** Forecast is always displayed (no toggle — showing forecast data is always valuable).

**KPI Row (5 cards):**

| KPI | Value | Colour | Trend |
|-----|-------|--------|-------|
| Active Volunteers | 1,247 | Blue | ▲ 312 new this year |
| Monthly Hours | 11,830 | Teal | ▲ 6.8% |
| Beneficiaries Served | 28,450 | Purple | ▲ 9.4% |
| Service Delivery Rate | 95% | Green | ▲ 2.1pp |
| Cost per Beneficiary | £390 | Amber | ▼ 3.2% (improving) |

**Charts:**

| Chart | Type | Span | Data |
|-------|------|------|------|
| Service Demand Trend & Forecast | Line chart with confidence band | span7 | 12-month historical + 3-month forecast with 95% CI shading (always visible) |
| Volunteer Hours by Programme | Stacked bar chart | span5 | Monthly volunteer hours split by programme |
| 7-Day Demand Forecast | Forecast card grid (7 cards) | span12 | Day, predicted sessions, confidence %, CI range |
| Resource Utilisation | Horizontal bar chart (`indexAxis:'y'`) | span6 | Staff, volunteers, centres, beds, slots — available vs deployed |
| Beneficiary Outcomes vs Targets | Horizontal bar chart (`indexAxis:'y'`) | span6 | Each outcome area: target bar vs actual bar |
| Volunteer Retention Trend | Line chart | span6 | Monthly retention rate over 12 months |
| Service Coverage Map | Leaflet map | span6 | 34 service delivery locations with circle markers sized by beneficiary volume |

**Additional elements:**
- **Demand drivers callout box**: Explaining seasonal factors (winter demand spike, school holidays, economic indicators, universal credit payment cycles) that affect the forecasting model

### 6.5 Dashboard Page — Benchmarks & Comparison

**Purpose:** Position Hope & Compass against sector benchmarks, demonstrating Simpson Associates' sector knowledge and data maturity assessment capability.

**Controls:**
- Benchmark source selector: NCVO Almanac / AAW Fundraising / M+R Digital / Charity Digital

**Charts:**

| Chart | Type | Span | Data |
|-------|------|------|------|
| KPI Benchmark Comparison | Grouped bar chart | span7 | Hope & Compass vs Sector Average vs Top Quartile for key metrics |
| Data Maturity Assessment | Radar chart | span5 | 7 Data Orchard dimensions: Data, Tools, Leadership, Skills, Culture, Uses, Analysis |
| Fundraising Efficiency Scatter | Scatter plot | span6 | Cost per £ raised (x) vs donor retention (y), Hope & Compass highlighted as larger circle |
| Income Diversification | Stacked bar chart | span6 | Income source mix for Hope & Compass vs 3 peer organisations |

**Data Maturity scores (Data Orchard framework, 1–5 scale):**

| Dimension | Hope & Compass | Sector Avg |
|-----------|---------------|-----------|
| Data | 3.4 | 2.8 |
| Tools | 3.1 | 2.5 |
| Leadership | 3.6 | 2.9 |
| Skills | 2.8 | 2.4 |
| Culture | 3.2 | 2.7 |
| Uses | 3.5 | 2.6 |
| Analysis | 2.9 | 2.3 |

### 6.6 Dashboard Page — AI Insights

**Purpose:** Showcase AI and advanced analytics capabilities with auto-generated recommendations across all three verticals.

**Filters:**
- Vertical: All / Fundraising / Partnerships / Operations
- Priority: All / Critical / High / Medium / Low

**Layout:** Dark-background panel (matching Police Hotspot AI Insights styling) with a 3-column grid of insight cards.

**Synthetic Insights (9 total, 3 per vertical):**

*(See Section 6.6 insights in original spec — all 9 insights are implemented as specified)*

### 6.7 Solutions Page

**Purpose:** Present Simpson Associates' NFP offerings as a solutions catalogue, aligned to Microsoft technology.

**Page hero:** "Our Not-For-Profit Solutions"

**Solution cards (6, in 3×2 grid):**

| # | Title | Description | Stats |
|---|-------|-------------|-------|
| 1 | Fundraising Analytics Platform | Donor data integration, segmentation, and personalisation model with real-time campaign dashboards. Built on Microsoft Fabric and Power BI. | "62%" Avg retention uplift, "4.5:1" Fundraising ROI |
| 2 | Partnership Intelligence Suite | Central repository for partnership data with AI-powered scoring model. | "47" Partners scored, "91%" Project completion |
| 3 | Operational Efficiency Platform | Volunteer data integration, service demand forecasting, and resource allocation. | "86%" Volunteer utilisation, "84%" Forecast accuracy |
| 4 | Nonprofit Data Accelerator | Pre-configured Azure + Fabric data platform with CDM for Nonprofits. Medallion lakehouse. | "90+" CDM entities, "3" Data tiers |
| 5 | AI & Advanced Analytics | Donor propensity models, partnership scoring, demand forecasting. Built on Azure ML. | "9" AI models, "84%" Avg accuracy |
| 6 | Data Strategy & Governance | Data maturity assessment, GDPR compliance, SORP 2026 reporting alignment. | "7" Maturity dimensions, "3" SORP tiers |

### 6.8 Case Studies Page

**Purpose:** Showcase real Simpson Associates case studies relevant to the NFP and social impact sector.

**Case study cards (4, in 2×2 grid):**

| # | Client | Description | Metrics | Tag |
|---|--------|-------------|---------|-----|
| 1 | **British Heart Foundation** | Databricks Data Intelligence Platform on Azure. Unified research data across national defibrillator network and RevivR CPR training app. H3 spatial indexing reduced analysis from 3+ days to 6 minutes. | "75%" Faster analysis, "1.5bn" Rows ingested | Data Platform |
| 2 | **Alzheimer's Society** | Azure Synapse and Power BI volunteer insights platform. Unified fragmented volunteer data across multiple systems for data-driven recruitment and retention. | "Unified" Volunteer view, "800k" People supported | Volunteer Analytics |
| 3 | **Commissioning Alliance** | Azure data warehouse serving 66 local authorities. Centralised SSDA903 children's social care data with Power BI self-service reporting. | "66" Local authorities, "SSDA903" Data unified | Data Platform |
| 4 | **Flagship Group** | Modern Data Analytics Assessment for 32,000-home housing association. Microsoft Fabric and medallion architecture roadmap with Purview governance. | "32,000" Homes managed, "Fabric" Roadmap | Strategy |

### 6.9 Contact Page

**Purpose:** Lead generation and demo booking.

**Left column — Form:**
- Name (text input, required)
- Email (email input, required)
- Organisation (text input, required)
- Organisation type (select: Charity / Social Enterprise / Foundation / Housing Association / NHS/Public Sector / Other)
- Area of interest (select: Fundraising Analytics / Partnership Intelligence / Operational Efficiency / Data Platform / AI & Advanced Analytics / Data Strategy / Full Suite Demo)
- Message (textarea)
- Submit button: "Request Demo"

**Right column — Info cards:**
- York Office: Suite 3, 20 George Hudson Street, York YO1 6WR
- Sheffield Office: 3 Concourse Way, Sheffield City Centre, Sheffield S1 2BJ
- Phone: +44 (0) 1904 234 510
- Website: www.simpson-associates.co.uk
- Accreditations: Microsoft Partner of the Year 2024, ISO 27001, ISO 9001, Cyber Essentials Plus, Databricks Partner

---

## 7. Interaction Patterns

### 7.1 Page Navigation

- **Top nav tabs** in header switch between the 4 top-level pages (Dashboard, Solutions, Case Studies, Contact)
- Active tab gets `active` class with blue background
- Page content shows/hides via `.page.active` toggling
- Function: `showPage(pageId, tabElement)`
- On mobile (≤700px), the "NFP Demo" tag is hidden and the nav is scrollable

### 7.2 Dashboard Panel Navigation

- **Dashboard sub-tabs** switch between the 6 panels within the dashboard page
- Active tab gets `active` class with blue background
- Panel content shows/hides via `.panel.active` toggling
- Panels animate in with `fadeUp` keyframe (opacity 0→1, translateY 12px→0)
- Each panel's charts are initialised on first view (lazy initialisation for performance)

### 7.3 Filter Controls

- **Select dropdowns** (`.fsel`) filter the data displayed in charts and tables
- Filters trigger chart data updates via Chart.js `.update()` method
- Filter state is local to each panel (not shared across panels)
- Chart references are obtained at invocation time via `Chart.getChart()` (deferred lookup for lazy init compatibility)

### 7.4 Toggle Switches

- **Toggle controls** (`.toggle`) are div-based elements that toggle an `.on` class on click
- Visual: 44×24px with white circle that slides right when active, background changes from grey (`--g300`) to blue (`--blue`)
- Smooth 0.3s CSS transition
- Toggles trigger chart reconfiguration — changing datasets, labels, or display options

### 7.5 Chart Interactivity

- **Hover tooltips** on all Chart.js charts showing exact values
- **Legend click** to show/hide individual datasets
- **Legend markers**: small filled circles (`usePointStyle:true`, `pointStyle:'circle'`) on all charts
- **Responsive resizing** via Chart.js `responsive: true, maintainAspectRatio: false`
- Consistent Chart.js configuration: no title (titles handled by card headers), matching font family, matching colour palette

### 7.6 Table Sorting

- **Partnership ranking table** and **donor segment table** support click-to-sort on column headers
- Sort indicator (▲/▼) shown in active column header
- Sort is client-side via array sort and DOM rebuild

### 7.7 Map Interaction (Operations)

- **Leaflet map** with CARTO Light tiles
- Circle markers for each of the 34 service delivery locations
- Marker size proportional to beneficiary volume
- Click marker for popup with location name and beneficiary count
- Map centred on Northern England (lat 53.8, lng -1.55, zoom 7)

---

## 8. Responsive Design

Following the Police Hotspot Landing Page breakpoints:

### Breakpoint: 1100px

| Component | Adaptation |
|-----------|-----------|
| Hero grid | Collapses to single column |
| KPI row | Changes to 2-column |
| Chart grid spans | All collapse to span 12 (full width) |
| Solution/insight grids | Collapse to 2-column |
| Case study grid | Collapses to single column |
| Contact grid | Collapses to single column |
| Hero stats | Changes from 4-column to 2-column |

### Breakpoint: 700px

| Component | Adaptation |
|-----------|-----------|
| Hero title | Reduces from 3.2rem to 1.5rem |
| KPI row | Collapses to single column |
| Forecast card grid | Changes from 7-column to 2-column |
| Demo tag | Hidden |
| Top nav | Compact with scrollable overflow |
| Header | Reduced height (56px) and padding |
| Solutions/case studies grids | Single column |
| Insight grid | Single column |

---

## 9. Alignment to TSI GTM Strategy

*(Unchanged from v1.0 — all GTM alignment items are implemented as specified)*

---

## 10. Microsoft Technology Alignment

*(Unchanged from v1.0 — all Microsoft technology references are implemented as specified)*

---

## 11. Implementation Phases

### Phase 1: Core Application (Complete)

**Deliverable:** Single HTML file (`index.html`) with all CSS, JS, and synthetic data inline.

**Implemented:**
- All 4 pages (Dashboard, Solutions, Case Studies, Contact)
- All 6 dashboard panels with full interactivity
- All charts, tables, maps, and filters
- Lazy chart initialisation (charts created on first panel view)
- Functional toggle switches and filter controls
- Sortable data tables
- Contact form validation
- 47 partner dataset
- Real Simpson Associates case studies
- Responsive design at 1100px and 700px breakpoints
- Simpson Associates branding (Silka font, colour system, logo SVG)

### Phase 2: Enhancements (Future)

- **Animated KPI counters** — numbers count up on page load
- **PDF export** — button to generate a PDF report from current dashboard view
- **Dark mode** — toggle for dark/light theme
- **Additional synthetic organisations** — selector to switch between 3 fictional charities of different sizes/types
- **Data maturity self-assessment** — interactive wizard that scores the visitor's own organisation
- **Embedded Power BI** — replace Chart.js with actual embedded Power BI reports (requires Power BI Embedded licence)

### Phase 3: Production Deployment (Future)

- **Azure Static Web Apps** hosting with custom domain
- **Application Insights** telemetry for tracking demo engagement
- **CRM integration** — form submissions routed to Dynamics 365 / HubSpot
- **A/B testing** — variant pages for different charity sub-sectors

---

## Appendices

### A. Glossary

| Term | Definition |
|------|-----------|
| CDM | Common Data Model — Microsoft's open-source data schema for nonprofits |
| SORP | Statement of Recommended Practice — UK charity accounting standard |
| LTV | Lifetime Value — total projected giving from a donor over the relationship |
| CAC | Cost of Acquisition — cost to acquire a new donor |
| SROI | Social Return on Investment — social impact measurement framework |
| TOMs | Themes, Outcomes and Measures — standardised social value framework |

### B. Data Sources for Benchmarks

| Source | URL | Data Used |
|--------|-----|-----------|
| NCVO UK Civil Society Almanac | ncvo.org.uk | Income, expenditure, overhead ratios |
| AAW Group Fundraising Benchmarks 2025 | aawpartnership.com | Fundraising efficiency metrics |
| M+R / Rally UK & Ireland Digital Benchmarks | mrbenchmarks.com/uk | Digital fundraising metrics |
| CAF UK Giving Report 2025 | cafonline.org | Household giving behaviour |
| Data Orchard Data Maturity Framework | dataorchard.org.uk | Data maturity dimensions and sector averages |
| Charity Digital Skills Report 2024 | charitydigital.org.uk | Data prioritisation statistics |
| Teque Research | teque.co.uk | CRM adoption, donor retention benchmarks |

### C. Simpson Associates Branding Assets

| Asset | Source |
|-------|--------|
| Silka font files | simpson-associates.co.uk/wp-content/themes/simpsons2024/assets/fonts/optimised/ |
| Logo SVG | Inline in header (391.04 × 97.15 viewBox) |
| Brand gradient | linear-gradient(-37deg, #8876E4 0%, #1E8BC8 98%) |
| Colour palette | CSS custom properties as documented in Section 4.2 |
