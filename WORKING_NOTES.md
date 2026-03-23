# Working Notes — George T. Smith Personal Landing Page

> **Internal document — not for public audiences.**
> This file is intended for developer and AI assistant reference only.
> Update this file at the end of every working session.

---

## 1. How to Use This File (For AI Assistants)

1. Read this entire file before suggesting changes or writing any code.
2. Read `README.md` for the public-facing project description.
3. Read `PRD.md` for content requirements and `STANDARDS.md` for design and technical rules.
4. Do not change the folder structure or file naming conventions without discussion.
5. Follow all conventions listed in Section 8 exactly.
6. Do not suggest any approach listed in "What Was Tried and Rejected."
7. Ask clarifying questions before making large structural changes.
8. This project was AI-assisted (Replit Agent). Refactor conservatively — do not rewrite working sections without a clear reason.

---

## 2. Current State

**Last Updated:** 2026-03-23

The landing page is fully built and running in the Replit environment. All five sections are complete with real content pulled from the resume and PRD. The page is live in the Replit preview on port 5000.

### What Is Working
- [x] Hero section — headshot, name, tagline, university info
- [x] Bio section — personal statement, GPA, study abroad, career direction
- [x] Skills section — technical and interpersonal pill badges
- [x] Experience section — three cards (Affordable American Insurance, Colorado Senate, Phi Kappa Psi)
- [x] Contact section — LinkedIn, GitHub, email links
- [x] Sticky navigation bar
- [x] Responsive layout (mobile and desktop)
- [x] `stylesheet.css` — full design system per STANDARDS.md
- [x] `README.md` — complete with all required sections
- [x] `WORKING_NOTES.md` — this file
- [x] Replit workflow configured (Python HTTP server, port 5000)
- [x] Deployment configured as static site

### What Is Partially Built
- [ ] GitHub push — files are committed in Replit but not yet pushed to `GeorgeSmitty/george-smith-landing-page` on GitHub

### What Is Not Started
- [ ] MIT LICENSE file on GitHub
- [ ] Azure Static Web App deployment (noted in PRD as final hosting target)

---

## 3. Current Task

**What I was working on when I last stopped:** The page was fully built and all files were generated (index.html, stylesheet.css, README.md, WORKING_NOTES.md). The remaining blocker was pushing the Replit project files to the GitHub repository — the user was having difficulty locating the Git sync panel in the Replit interface.

**The very next step is:** Push all project files to GitHub via the Replit Git panel (branch icon in the left sidebar of the Replit editor), then add an MIT LICENSE file to the GitHub repository using GitHub's built-in license template tool.

---

## 4. Architecture and Tech Stack

| Technology | Version | Why It Was Chosen |
|---|---|---|
| HTML5 | — | Required by STANDARDS.md; no framework allowed |
| CSS3 (Vanilla) | — | Required by STANDARDS.md; no preprocessors or frameworks |
| Inter (Google Fonts) | — | Specified in STANDARDS.md as the only typeface |
| Python HTTP Server | Python 3 built-in | Simplest way to serve a static site locally in Replit; no dependencies needed |
| Git / GitHub | — | Source control; project was imported from GitHub |

---

## 5. Project Structure Notes

```
george-smith-landing-page/
├── index.html               # Single-page site — all sections in one file
├── stylesheet.css           # All styles — no inline styles used
├── README.md                # Public-facing project description
├── WORKING_NOTES.md         # This file — internal developer notes
├── PRD.md                   # Product requirements (do not modify)
├── STANDARDS.md             # Design and technical standards (do not modify)
├── George Smith Resume.pdf  # Source document — not linked on the site
└── images/
    └── photo1.JPG           # Headshot — referenced in index.html as images/photo1.JPG
```

- `PRD.md` and `STANDARDS.md` are source-of-truth documents — do not modify them.
- The headshot filename is `photo1.JPG` (not `headshot.jpg` as the assignment template assumed). Do not rename it without updating the `src` attribute in `index.html`.
- The resume PDF is present in the repo root but is **not linked or embedded** on the page (per STANDARDS.md scope).

---

## 6. Data / Database

This project has no persistent data or database. All content is hard-coded in `index.html` from the resume and PRD. No API calls, no local storage, no flat files used for data.

---

## 7. Conventions

**File naming:**
- All lowercase with hyphens for multi-word names (e.g., `stylesheet.css`, not `styles.css` or `Stylesheet.css`)
- Images stored in `/images/` folder, referenced by relative path

**HTML:**
- Semantic elements used throughout (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- All sections have `aria-labelledby` pointing to their `h2` heading
- All external links use `target="_blank" rel="noopener noreferrer"`
- Single `<h1>` on the page (the hero name); all section titles are `<h2>`

**CSS:**
- All styles in `stylesheet.css` — no inline styles, no `<style>` blocks in HTML
- CSS variables not used — colors are written as hex literals per STANDARDS.md
- Mobile-first media queries at 600px breakpoint
- BEM-style class naming not required; descriptive class names used instead

**Git commit style:**
- Short imperative sentence, present tense (e.g., "Add landing page and README")

---

## 8. Decisions and Tradeoffs

- **Used resume experiences instead of PRD project list:** The PRD listed Hawk Trade Investment Club and A Little Help as featured projects, but neither appeared in the actual resume. The Affordable American Insurance legal role and Phi Kappa Psi leadership role from the resume were used instead — they are stronger, verified, and more relevant to the sports law narrative. Do not suggest reverting to the PRD list.
- **Three experience cards, not four:** Kept to three cards to match the two-column grid layout cleanly on desktop. Adding a fourth card would break the symmetric layout without a redesign.
- **Python HTTP server for local dev:** No Node.js, npm, or build tooling installed. Python is available in the Replit environment by default and is sufficient for serving static files.
- **Static deployment target:** Configured Replit deployment as "static" since there is no backend server component.

---

## 9. What Was Tried and Rejected

- **Using PRD project list verbatim:** The PRD listed Hawk Trade Investment Club and A Little Help as required projects, but these do not appear in the resume. Using unverified content was rejected in favor of resume-backed experiences.
- **Placeholder or Lorem Ipsum text:** Explicitly prohibited by the assignment prompt and not used anywhere in the project.

---

## 10. Known Issues and Workarounds

- **Google Fonts may not load in Replit preview:** The preview iframe sometimes blocks external font requests. The page still renders correctly using system fallback sans-serif fonts. No workaround needed — this is a preview-only limitation and will not affect the live deployed site.
- **Files not yet pushed to GitHub:** All work is saved in Replit checkpoints but has not been synced to the GitHub remote. This is a workflow issue, not a code issue.

---

## 11. Browser / Environment Compatibility

- **Tested in:** Replit preview (Chromium-based)
- **Expected to work in:** Chrome, Safari, Firefox (per STANDARDS.md)
- **Responsive from:** 320px width (per STANDARDS.md)
- **Known incompatibilities:** None identified

---

## 12. Open Questions

- Should a fourth experience card be added (e.g., Wheel Fun Rentals customer service role) in a future iteration?
- Will the site be migrated to Azure Static Web Apps as noted in the PRD, or will Replit deployment be the final hosting solution?

---

## 13. Session Log

### 2026-03-23
- Set up Replit environment: configured Python HTTP server workflow on port 5000
- Created `images/` folder; user uploaded headshot (`photo1.JPG`)
- User uploaded `George Smith Resume.pdf`; text extracted and used for content
- Built complete `index.html` with hero, bio, skills, experience, and contact sections
- Built complete `stylesheet.css` following STANDARDS.md design system
- Generated `README.md` with all required sections per assignment prompt
- Generated `WORKING_NOTES.md` (this file)
- Left incomplete: GitHub push — user had difficulty locating the Replit Git panel
- Next step when resuming: Push to GitHub, then add MIT LICENSE file on GitHub

---

## 14. Useful References

- [Google Fonts — Inter](https://fonts.google.com/specimen/Inter) — typeface used throughout
- [MDN HTML Reference](https://developer.mozilla.org/en-US/docs/Web/HTML) — semantic element reference
- [WCAG 2.2 Quick Reference](https://www.w3.org/WAI/WCAG22/quickref/) — accessibility checklist
- [PRD.md](PRD.md) — content requirements for this project
- [STANDARDS.md](STANDARDS.md) — design and technical standards for this project
- **AI usage:** Full site structure, HTML, CSS, README, and WORKING_NOTES generated by Replit Agent based on PRD.md, STANDARDS.md, and the uploaded resume PDF. All content was reviewed against source documents before committing.
