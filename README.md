# ug-content

Shared, version-controlled content blocks for the Math Department undergraduate webpages.

**Purpose.** This repo stores the *stable* (low-volatility) text that we want to be able to:
- draft and review in GitHub,
- reuse in two prototypes:
  - a **university-site prototype** (binghamton.edu-style pages),
  - a **department-site prototype** (math dept “current students” hub),
- and then migrate into the official university CMS without copy/paste drift.

This repo intentionally contains **content only** (mostly Markdown), not site design.

---

## Content contract (important)

1) **One canonical home per topic.**  
Every file declares whether its canonical home is `university` or `department`.  
The *non-canonical* site should **not** duplicate full text — it should link to the canonical location.

2) **Stable only.**  
This repo is for content that changes rarely (typically once per year or less).  
Anything that changes within a semester (deadlines, advising logistics, offerings, petitions) belongs on the departmental site.

3) **Review cadence.**  
Each file includes a `Last reviewed` date. A yearly review pass is expected.

---

## File metadata (required)

At the top of every Markdown file, include these three lines:

Owner: Math UG Program  
Canonical: university | department  
Last reviewed: YYYY-MM-DD  

Example:

Owner: Math UG Program  
Canonical: university  
Last reviewed: 2025-12-22  

---

## Suggested structure

- `overview/` — program overview, learning outcomes, research/careers blurbs (evergreen)
- `tracks/` — track descriptions (narrative; avoid semester-specific details)
- `policies/` — stable policies/FAQs (avoid deadlines and staffing-dependent info)
- `assets/` — only if needed (avoid BU trademarks/logos unless cleared)

---

## Writing guidelines (to avoid drift and fragility)

- Prefer **descriptions** over brittle checklists.
- If listing requirements, prefer phrasing like “typically includes …” and link to the official catalog/guide for the authoritative list.
- Avoid:
  - course rotation promises (“offered every spring”),
  - named staff contacts (these change),
  - dates and deadlines (these change),
  - “how to petition” instructions (these change).

---

## How this repo is used

This repo is consumed by two separate site prototypes:
- `ug-university-prototype` (static content pages + links to dept hub for current-student logistics)
- `ug-dept-prototype` (dynamic hub + links to university pages for stable descriptions)

Technically, each site repo can include this repo as a **git submodule** (preferred) or as a synced folder.

---

## Contribution / workflow

- Small PRs are preferred.
- When updating content, update the `Last reviewed` date.
- Use clear commit messages (e.g., “Revise Actuarial track description”).
- If a topic’s canonical home changes, change the `Canonical:` line and ensure the other site will link rather than duplicate.

---

## Notes

- Treat this as drafting/prototyping content that will later be migrated into the official university CMS.
- Avoid uploading BU branding assets unless explicitly approved.
