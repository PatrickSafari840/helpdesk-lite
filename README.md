# HelpDesk Lite

**A lightweight IT service desk: priority matrix, SLA timers, Kanban board, metrics and a troubleshooting knowledge base.**

🔗 **Live demo:** https://patricksafari840.github.io/helpdesk-lite/

Small companies often run IT support through phone calls and WhatsApp messages, so nothing is tracked and urgent problems wait behind small ones. HelpDesk Lite shows how a simple service desk works, applying what I learned in the Google IT Support and Google Project Management certificates.

## Features

- **ITIL-style priority matrix**: impact (one person / a team / the whole company) × urgency gives P1–P4 automatically.
- **SLA timers**: each priority has a resolution target (P1 4 h, P2 8 h, P3 24 h, P4 72 h). Cards show time left, turn amber when at risk and red when breached.
- **Kanban board**: New → In progress → Waiting on user → Resolved. Drag and drop, filter by priority or technician, search.
- **Ticket details**: requester, department, assignee, activity log, notes, and a suggested fix from the knowledge base.
- **Metrics**: open tickets by priority, % resolved within SLA, mean time to resolve (MTTR), tickets breaching now, tickets by category, opened vs resolved trend.
- **Knowledge base**: step-by-step first-line fixes (Wi-Fi/DNS, printers, slow PCs, locked accounts, email, phishing, crashing apps).
- **Bilingual EN/FR**, light/dark theme, works on phones.

The app starts with ~50 realistic demo tickets spread over the last 4 weeks; use *Reset demo* in the footer to regenerate them. Data is stored in the browser (`localStorage`); there is no server.

## Tech

Plain HTML, CSS and JavaScript in a single file: HTML5 drag and drop, hand-drawn SVG charts, no framework, no build step.

## Run locally

```bash
git clone https://github.com/PatrickSafari840/helpdesk-lite.git
cd helpdesk-lite
python -m http.server 8000   # then open http://localhost:8000
```

## Possible next steps

- Backend API (Node.js/Express + PostgreSQL) with technician logins
- Email-to-ticket and WhatsApp notifications on SLA risk
- Business-hours SLA calendar

---

Built by **Patrick Safari**, full stack developer & IT specialist in Goma, DR Congo · [Portfolio](https://patricksafari840.github.io/patrick_safari_portfolio/) · [LinkedIn](https://www.linkedin.com/in/patrick-safari-166077255/)

Licensed under the MIT License.
