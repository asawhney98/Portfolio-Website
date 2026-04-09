# CLAUDE.md — Aayush Sawhney Portfolio

This file tells Claude (and any AI assistant) exactly how to work on this project.
Read this before touching any file.


This is the link where the site is currently hosted [via github pages: https://asawhney98.github.io/Portfolio-Website/]
---

## Project Overview

A single-file personal portfolio website for Aayush Sawhney, Senior Product Manager.
Audience: EU and global hiring managers, recruiters, founders.
Primary job: Convert portfolio visits into interview conversations — fast.

**Stack:** Pure HTML + CSS + vanilla JS. Zero frameworks. Zero build steps.
**Single file:** `index.html` — everything lives here.

---

## File Structure

```
/
├── index.html          ← The entire portfolio. Do not split this.
├── CLAUDE.md           ← This file
└── README.md           ← GitHub repo description (auto-generated)
```

Do not introduce React, Tailwind, npm, or any build tooling.
Do not split CSS into separate files unless explicitly asked.
Do not add new pages — the tabbed SPA structure is intentional.

---

## Design System (do not deviate without asking)

| Token | Value |
|---|---|
| `--cream` | `#F8F5F0` — page background |
| `--parchment` | `#EDE8DF` — subtle surfaces |
| `--ink` | `#1A1714` — primary text |
| `--ink-light` | `#4A4540` — body text |
| `--ink-muted` | `#8A847C` — labels, metadata |
| `--accent` | `#B85C38` — terracotta, all interactive elements |
| `--accent-light` | `#F0E6E0` — accent fills |
| `--rule` | `#D4CEC5` — borders and dividers |
| Display font | Playfair Display (serif) — headings, numbers |
| Body font | DM Sans — all UI text |

**Tone:** Editorial, warm, professional. Not techy/dark. Not corporate/blue.
**Do not** introduce gradients, shadows, dark backgrounds, or new fonts.

---

## Content Rules

### Voice & Tone
- First-person implied, not stated ("Led 13-member team" not "I led")
- Metrics-first: lead every bullet with the outcome number
- No fluff phrases: "passionate about", "results-driven", "synergy"
- Brutal brevity: if a sentence can be cut, cut it

### Keyword Integrity (EU PM hiring — do not remove these)
These terms must remain visible in the page at all times:
`Agentic AI · LLMs · MCP · Model Context Protocol · GenAI Platform · RAG ·
Multi-Agent Workflows · Fraud Risk · FinTech · Cloud-Native · OKRs · EU GDPR`

They appear in: meta keywords, keyword banner, skill cells, project tags.
If you refactor any section, verify these survive.

### Metrics (do not alter without owner confirmation)
| Claim | Source |
|---|---|
| $200M+ annual impact | MaaS Platform projected impact, Amex |
| 75% time-to-market reduction | 30 days → 7 days, Model-in-a-Box |
| 150+ ML models | Platform adoption, Amex SGP |
| +22% DAU | Offers personalisation launch |
| 73% fraud improvement | Suspect Dispute Management |
| $10M+ tax incentives | SGP–US ML validation framework |

---

## Navigation Architecture

```
Nav
├── About Me
│   ├── Résumé        (default active tab)
│   ├── Side Projects
│   └── Product Philosophy
└── Resources
    ├── Recommendations
    └── PM Resources
```

Tab switching is handled by showPanel(), showSub(), showResourceSub() in the
inline <script> at the bottom of index.html. Keep all JS inline.

---

## What Needs Updating (owner action items)

- [ ] LinkedIn URL in contact strip (currently placeholder /in/)
- [ ] 3 x Recommendation quotes — replace placeholder cards with real text
- [ ] Projects 03 and 04 — fill in when ready; remove placeholder class
- [ ] "My Thinking" articles — expand each into a linked Notion page or blog post
- [ ] Add og:image meta tag once a headshot or OG image is created

---

## Hosting

**Live at:** https://<your-github-username>.github.io
**Repo name must be:** <your-github-username>.github.io
**Branch:** main
**GitHub Pages source:** root / on main

To update the live site: edit index.html → commit → push to main.
GitHub Pages auto-deploys within ~60 seconds.

---

## Common Tasks for Claude

### Add a new Side Project
1. Copy an existing .project-card block in index.html
2. Remove the placeholder class and pointer-events: none style
3. Fill in: project-type, project-name, project-desc, project-tag spans
4. Add href to the <a> tag
5. Verify keyword tags include at least one required EU PM keyword

### Add a Recommendation
1. Copy a .rec-card block
2. Replace quote text, name, and title
3. Keep quote under 3 sentences — specific outcomes beat generic praise

### Update a Metric
1. Check the metrics table above to confirm the source
2. Update both the hero .metric-num AND the relevant experience bullet
3. Never fabricate or round up — these are cited in interviews

### Change a Colour
1. Update the CSS variable in :root only
2. Do not hardcode hex values anywhere in the file
3. Test in both light and dark browser backgrounds

---

## What Claude Should NOT Do

- Do not add authentication, forms, or backend calls
- Do not introduce localStorage or sessionStorage
- Do not split into multiple HTML files
- Do not add a cookie banner (no tracking by default)
- Do not remove the keyword banner — intentional for ATS/SEO
- Do not alter metrics without explicit owner confirmation
- Do not suggest migrating to React, Next.js, or any framework
- Do not add a photo without explicit instruction

---

## Adding Analytics (optional, owner decision)

If the owner wants to track visits, add this before </head> and nowhere else:

  <!-- Plausible: privacy-friendly, no cookies, EU GDPR compliant -->
  <script defer data-domain="yourdomain.com" src="https://plausible.io/js/script.js"></script>

Do not use Google Analytics without explicit consent — EU GDPR applies.

---

Last updated: April 2026
Owner: Aayush Sawhney — asawhney98@gmail.com
