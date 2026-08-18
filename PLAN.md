# PLAN — SEO optimization

**Context:** New client request — improve the SEO of this static website (Zonnestroom
Baarn, a Dutch solar-panel installer). The site currently has significant on-page /
technical SEO gaps.

**Goal:** Measurably improve the site's SEO. Work in visible, measurable steps and
report back at each step. Do **not** change the visible design.

## Step 1 — Serve & baseline
- Start a local server from the repo root: `python -m http.server 8000` (or `npx serve`).
- Confirm the site loads at http://localhost:8000.
- Run Lighthouse (SEO category only) on the homepage, record the baseline score + top
  failing audits:
  ```
  npx lighthouse http://localhost:8000/index.html --only-categories=seo --quiet \
    --chrome-flags="--headless" --output=html --output-path=./before.html
  ```

## Step 2 — Audit & plan
List the concrete on-page / technical SEO issues, e.g.:
- Missing `<title>` and meta description
- No `<meta name="viewport">`, charset, or `lang`
- No real `<h1>` / heading hierarchy (headings are styled `<div>`s)
- Images without `alt`; vague anchor text ("Klik hier")
- No canonical; no Open Graph / Twitter tags
- No JSON-LD structured data (LocalBusiness)
- No `robots.txt` / `sitemap.xml`; non-semantic markup

Write a short plan for the fixes.

## Step 3 — Implement
Apply every fix across all HTML pages. Add `robots.txt` and `sitemap.xml`.
Keep the visible design unchanged. Commit as **"SEO fixes"**.

## Step 4 — Re-score
Re-run the same Lighthouse command → `./after.html`. Report the **before → after SEO
score** and confirm which issues are now resolved.

---
_Follow-up (on request): package this exact procedure as a reusable Agent Skill._
