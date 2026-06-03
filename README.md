# PlayerOne — CARO Governance Simulation Platform

**Live platform → [playerone.carononprofit.org](https://playerone.carononprofit.org)**

PlayerOne is an 8-stage civic leadership and governance simulation platform built for [CARO](https://carononprofit.org) (Care for Assets, Resources, and Obligations) — a US 501(c)(3) nonprofit operating across Bangladesh.

The platform activates citizens through a structured pipeline: from governance awareness to verified civic leadership, with AI-assisted evaluation at every stage. Bangladesh is the proof of concept. The architecture is designed to replicate to any governance context.

---

## What the Platform Does

Citizens enter an 8-stage journey — each stage requires real work, not just coursework. Progress is gated, AI-scored, and verified.

| Stage | Name | What the Participant Does |
|---|---|---|
| 0 | Fairness Index (FI) | Rates governance fairness across 5 domains — produces live research data |
| 1 | MEP — Civic Education | Foundational modules and written reflections on personal fairness experience |
| 2 | VEP — Civic Experience | 12-week applied program in a chosen department with AI-scored submissions and completion certificate |
| 3 | CMEP — Community Research | Field sessions documenting governance fairness on the ground |
| 4 | BIP — Balance Improvement | Extended project to improve fairness in a specific civic domain |
| 5 | CA — Campus Ambassador | Sustained outreach distributing the Fairness Index across a constituency |
| 6 | NEXUS | Original governance research and peer review |
| 7 | EL — Equitism Leader | Verified civic leadership designation — built and measured, not claimed |

---

## Technical Architecture

### Backend
- **Supabase** — PostgreSQL database with Row Level Security (RLS)
- **33 tables** — participants, progress tracking, submissions, research data, certificates, steward assignments
- **4 Edge Functions** — AI scoring, certificate generation, notifications, data export
- **Multi-role auth** — participant / admin / steward / journey-admin

### Authentication
- Google OAuth
- SMS OTP
- Email OTP
- Session persistence with role-based route guards

### AI Integration
- **Anthropic API** — Claude-powered evaluation of civic submissions
- **8 scoring rubrics** — one per stage, tailored to stage deliverables
- **Bangla and Banglish support** — evaluates submissions in both languages
- Scores stored in Supabase with full audit trail

### Frontend
- 50+ HTML pages — pure HTML/CSS/JavaScript
- Bilingual UI — Bengali and English throughout
- Custom design system with CSS variables and component tokens
- Admin dashboard — participant management, intelligence panel, scenario editor
- VEP workbook — 12-week structured content delivery system

### Data & Research
- Live Fairness Index data collection — feeds CARO's governance research program
- Google Apps Script export pipeline
- Google Drive integration for research data
- GA4 analytics
- Union-Find deduplication algorithm for participant verification across constituencies

### Infrastructure
- Deployed on Namecheap cPanel hosting
- Supabase cloud backend
- Brevo transactional email via Edge Function
- Custom subdomain architecture

---

## Research Output

PlayerOne generates live governance research data through the Fairness Index (FI) instrument — a 25-question civic measurement tool across 5 domains.

| Metric | Figure |
|---|---|
| Pilot sample (FI V1) | N=86, April 2026 |
| Live platform sample | N=43, ongoing |
| Overall Fairness Index — pilot | 1.74 / 5.0 |
| Overall Fairness Index — live platform | 1.30 / 5.0 |
| Domains measured | 5 — Governance, Justice & Rule of Law, Economy, Public Services, Accountability |
| Geographic coverage | 211 of 300 Bangladesh parliamentary constituencies |

Two independent samples converging at 1.74 and 1.73 — early validity signal for the instrument. Published baseline: SSRN #6632960.

---

## Built By

**A N M Nuruddin** — Founder & Chief Architect, CARO
- MS — Information Systems Security, University of the Cumberlands (2025)
- Author, *Fairness as Foundation: A Complete Architecture for Structurally Fair Governance* (2026)
- Published governance research: Fairness Index V1, N=86, Bangladesh (2026)

📧 anm.nuruddin@gmail.com · 🌐 [carononprofit.org](https://carononprofit.org) · [caroglobal.org](https://caroglobal.org)

---

## Status

Platform is in active production. V2.0 development ongoing.
This repository contains documentation only — production codebase is maintained privately for security.
