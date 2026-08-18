# SEO audit — Zonnestroom Baarn (agent-generated)

## Findings (on-page / technical)
| # | Issue | Impact |
|---|---|---|
| 1 | No `<title>` on any page | High — the single biggest ranking + click-through signal |
| 2 | No meta description | High — controls the search snippet |
| 3 | No `<meta name="viewport">` | High — hurts mobile ranking |
| 4 | No `<meta charset>` | Medium — encoding/rendering correctness |
| 5 | No `lang` attribute on `<html>` | Medium — language targeting |
| 6 | No real `<h1>` (headings are `<div class="big">`) | High — no heading hierarchy for crawlers |
| 7 | Images have no `alt` text | Medium — accessibility + image SEO |
| 8 | Vague anchor text ("Klik hier") | Medium — link context |
| 9 | No canonical URLs | Medium — duplicate-content protection |
| 10 | No Open Graph / Twitter cards | Medium — link previews on socials |
| 11 | No structured data (JSON-LD LocalBusiness) | High — rich results, local pack |
| 12 | No `robots.txt` | Medium — crawl directives |
| 13 | No `sitemap.xml` | Medium — discovery of all pages |
| 14 | Non-semantic layout (`div` soup) | Low/Med — semantics aid crawlers + a11y |

## Plan
Rewrite both pages with: `lang`, charset, viewport, unique title + meta description, single
`<h1>` + `<h2>`s, semantic `header/nav/main/footer`, `alt` on all images, descriptive anchors,
canonical, OG/Twitter tags, and JSON-LD `LocalBusiness`. Add `robots.txt` + `sitemap.xml`.
