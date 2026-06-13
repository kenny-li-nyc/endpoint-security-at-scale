# Project Reference: Endpoint Security at Scale

## What this project is

A professional static white paper website hosted on GitHub Pages.
It is authored by Kenny Li, Senior Infrastructure Engineer.
It reads as a technical reference document, not a personal blog or study guide.
It is intended to be shared with hiring managers and technical teams.

Live URL: https://kenny-li-nyc.github.io/endpoint-security-at-scale
Repo: https://github.com/kenny-li-nyc/endpoint-security-at-scale

---

## File structure

```
index.html          Homepage with hero and 5-layer architecture overview
layer1.html         Layer 01: Windows & Azure Platform
layer2.html         Layer 02: Telemetry Collection
layer3.html         Layer 03: Detection & Analytics
layer4.html         Layer 04: Security Copilot
layer5.html         Layer 05: Automated Response
operations.html     How the 5 layers work together end-to-end
assets/style.css    Single shared stylesheet for all pages
assets/nav.js       Mobile nav toggle behavior
PROJECT.md          This file
CONTENT.md          Full content outline for all pages
README.md           Explains the project and the AI-assisted build process
```

---

## Technology constraints

- Plain HTML, CSS, and vanilla JavaScript only
- No CSS frameworks (no Bootstrap, no Tailwind)
- No JavaScript frameworks (no React, no Vue)
- Google Fonts: Inter (weights 400 and 600) loaded via link tag
- Mobile responsive, breakpoint at 768px
- No linting. Do not run linters. Do not attempt to fix lint errors.

---

## Color system (CSS custom properties in assets/style.css)

```css
--navy-dark: #0a1628       /* top navigation bar background */
--navy-mid: #0d1f3c        /* hero section background */
--navy-border: #1e3a5f     /* borders inside navy sections */
--accent-blue: #4ea8de     /* tech card headings, links */
--accent-teal: #1D9E75     /* section tags, active sidebar item, hover accents */
--text-primary: #1a1a2e    /* all body text */
--text-muted: #5a6a7a      /* secondary text, captions, card descriptions */
--border-light: #e2e8f0    /* section dividers, card borders */
--bg-surface: #f8fafc      /* sidebar background, tech card backgrounds */
```

---

## Page layout structure

Every page except index.html uses this structure:

```
navbar
  page-layout
    sidebar (250px, lists all 5 layers with active highlight)
    page-content
      page-hero (navy background, layer eyebrow + title + purpose)
      page-body
        content-block (section tag + h2 + paragraphs or tech-grid)
        content-block
        ...
footer
```

index.html uses:
```
navbar
hero (full width navy)
main.container
  layer-grid (5 cards)
  content sections
footer
```

---

## CSS classes to use consistently

### Sidebar
- `.sidebar` on the aside element
- `.active` on the current page link
- Each sidebar link shows the layer number and title

### Page hero
- `.page-hero` wraps the navy header area
- `.layer-eyebrow` for the "Layer 01" label above the title
- `.purpose` for the one-sentence purpose statement below the h1

### Content sections
- `.content-block` wraps each section (tag + heading + content)
- `.section-tag` for the small uppercase label above each h2
- `.intro` class on the first paragraph of a section (slightly larger, muted)
- `.pipeline-note` for the dark navy callout box at the end of each layer page

### Technology cards
- `.tech-grid` wraps the card grid
- `.tech-card` for each individual card
- Card structure: h4 (blue heading) + p (muted description)

---

## Design principles

1. Generous whitespace. Each content-block has padding-top: 3rem.
2. Max content width of 720px inside content blocks to keep line length readable.
3. Paragraph line-height of 1.8 for readability.
4. Section tags (small teal uppercase labels) visually separate each section.
5. The pipeline-note callout at the end of each layer page connects it to the next layer.
6. Cards use bg-surface background and border-light border, never white-on-white.
7. No hover animation that moves elements (no translateY). Use border-color change only.

---

## Writing style rules

These rules are non-negotiable. Every sentence of content must follow them.

1. NO dashes of any kind. Not em dashes, not hyphens used as pauses. Zero.
2. Short sentences. One idea per sentence. Maximum 20 words per sentence.
3. No sentence should contain more than two clauses.
4. Do not use the word "leveraging". Do not use "utilizing". Do not use "seamlessly".
5. Do not pack three concepts into one sentence. Split them.
6. Do not use transitional filler phrases like "It is worth noting that" or
   "This is particularly important because".
7. Write like a senior engineer explaining something to a peer. Direct. Clear. Specific.
8. Avoid passive voice where possible. Say who does what.
9. Paragraphs are 2 to 4 sentences. No longer.
10. Tech card descriptions are 2 sentences maximum.

### Example of bad writing (do not do this)
"Active Directory controls authentication, authorization, and group membership
across domain-joined endpoints — making it the authoritative identity store
for on-premises environments that security teams depend on."

### Example of good writing (do this)
"Active Directory is the authoritative identity store for on-premises
environments. It controls authentication, authorization, and group membership
across domain-joined endpoints."

---

## Navigation links (same on every page)

```html
<li><a href="index.html">Overview</a></li>
<li><a href="layer1.html">Architecture</a></li>
<li><a href="tools.html">Tools & Platforms</a></li>
<li><a href="operations.html">Operations</a></li>
```

---

## Footer (same on every page)

```html
<footer>
  <div class="container">
    <p>Kenny Li · Senior Infrastructure Engineer · github.com/kenny-li-nyc</p>
  </div>
</footer>
```

---

## Sidebar (same on every layer page, change active class per page)

```html
<aside class="sidebar">
  <h4>Architecture Layers</h4>
  <ul>
    <li><a href="layer1.html">01 Windows & Azure Platform</a></li>
    <li><a href="layer2.html">02 Telemetry Collection</a></li>
    <li><a href="layer3.html">03 Detection & Analytics</a></li>
    <li><a href="layer4.html">04 Security Copilot</a></li>
    <li><a href="layer5.html">05 Automated Response</a></li>
  </ul>
</aside>
```

Add class="active" to the link matching the current page.

---

## README summary (for reference)

This site was researched, structured, and authored by Kenny Li.
It was built using Aider with Gemini Flash as the AI coding assistant.
The content reflects 13 years of enterprise Windows and Azure infrastructure
experience applied to the endpoint security domain.