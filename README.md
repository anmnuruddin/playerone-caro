# PlayerOne — CARO Governance Simulation Platform

**Live platform → [playerone.carononprofit.org](https://playerone.carononprofit.org)**

A 7-stage civic leadership and governance simulation platform built for [CARO](https://carononprofit.org) (Care for Assets, Resources, and Obligations) — a US 501(c)(3) nonprofit operating across Bangladesh.

PlayerOne activates citizens through a structured pipeline: from governance awareness to trained civic volunteers, with AI-assisted evaluation at every stage.

---

## What the Platform Does

Citizens enter a 7-stage journey:

| Stage | Name | What Happens |
|---|---|---|
| 0 | Fairness Index (FI) | Citizen rates governance fairness across 5 domains — produces live research data |
| 1 | MEP — Mirror Exercise Protocol | Structured reflection on governance experience |
| 2 | VEP — Volunteer Engagement Program | 12-week civic training with AI-scored submissions and completion certificate |
| 3 | CMEP — Community Mobilization | Community-level activation and organizing |
| 4 | BIP — Bangladesh Institute Program | Track-based advanced civic leadership (3 tracks) |
| 5 | CA — Constituency Assembly | Constituency-level civic governance building |
| 6 | NEXUS | Peer review, endorsement, and stewardship |

---

## Technical Architecture

### Backend
- **Supabase** — PostgreSQL database with Row Level Security (RLS)
- **33 tables** — participants, progress tracking, submissions, research data, certificates, steward assignments
- **4 Edge Functions** — AI scoring, certificate generation, notifications, data export
- **Multi-role auth** — participant / admin / steward / journey-admin

### Authentication
- Google OAuth
- SMS OTP (phone-based entry)
- Email OTP
- Session persistence with role-based route guards

### AI Integration
- **Anthropic API** — Claude-powered evaluation of civic submissions
- **8 scoring rubrics** — tailored per stage and track
- **Bangla and Banglish support** — evaluates submissions in both languages
- Scores stored in Supabase with full audit trail

### Frontend
- 50+ HTML pages — pure HTML/CSS/JavaScript, no framework dependency
- Bilingual UI — Bengali and English throughout
- Custom design system with CSS variables and component tokens
- Admin dashboard — participant management, intelligence panel, scenario editor
- VEP workbook — 12-week structured content delivery

### Data & Research
- Live Fairness Index data collection — feeds CARO's governance research program
- Google Apps Script export pipeline
- Google Drive integration for research data
- GA4 analytics
- Deduplication logic using Union-Find algorithm for participant verification

### Infrastructure
- Deployed on Namecheap cPanel hosting
- Supabase cloud backend
- Brevo transactional email (Edge Function integration)
- Custom subdomain architecture — playerone / admin / separate stage routes

---

## Research Output

PlayerOne generates live governance research data through the Fairness Index instrument.

| Metric | Figure |
|---|---|
| Pilot sample (FI V1) | N=86, April 2026 |
| Live platform sample | N=43, ongoing |
| Overall Fairness Index (OFI) | 1.74 / 5.0 (pilot) · 1.73 / 5.0 (live) |
| Domains measured | 5 — Governance, Justice, Economy, Public Services, Accountability |
| Geographic coverage | 211 of 300 Bangladesh parliamentary constituencies |

Two independent samples converging at 1.74 and 1.73 — early validity signal for the instrument.

---

## Built By

**A N M Nuruddin** — Founder & Chief Architect, CARO
- MS — Information Systems Security, University of the Cumberlands (2025)
- Author, *Fairness as Foundation: A Complete Architecture for Structurally Fair Governance* (2026)

📧 anmnuruddin@carononprofit.org
🌐 [carononprofit.org](https://carononprofit.org) · [caroglobal.org](https://caroglobal.org)

---

## Status

Platform is in active production. V2.0 development ongoing.
This repository contains documentation only — production codebase is maintained privately for security.
