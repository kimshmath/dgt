# Dynamical Group Theory — conference series website

This repository hosts **https://dgt.ggt.kr** via GitHub Pages.

The site is a single self-contained page: [`index.html`](index.html) (all CSS/JS inline,
no build step). **Any push to `main` deploys automatically** within a minute or two.

## How to add a new event

Events live in `index.html` inside `<ol class="timeline">`, newest first.
Copy an existing `<li class="event">` block and edit it:

```html
<li class="event reveal">
    <span class="roman">IX</span>
    <p class="event-name">Dynamical Group Theory IX</p>
    <p class="event-theme">Optional one-line theme (italic serif)</p>
    <p class="event-meta">
        <span class="date">Month D – D, YYYY</span>
        <span class="sep">·</span>
        <span>Venue, City, Country</span>
    </p>
    <a class="event-link" href="https://..." target="_blank" rel="noopener">Website ↗</a>
</li>
```

- Keep the list in **reverse-chronological order** (newest at the top).
- `event-theme` is optional — delete the line if the edition has no separate theme.
- For a dead/offline event page, link a Wayback Machine snapshot instead and use
  `class="event-link archived"` with the label `Archived site ↗`.
- The **Upcoming** banner is the `<div class="upcoming">` block near the top —
  update it when the next edition is announced, and move the previous "upcoming"
  event into the timeline once it has taken place.

## Conventions

- Dates use en dashes with spaces: `January 6 – 8, 2026`.
- Multi-day events: write the full range; the list is ordered by end date.
- Please verify dates/venues against the event's own page before editing —
  the series history was reconstructed from primary sources in August 2026.

## Domain

`dgt.ggt.kr` is configured via the `CNAME` file (do not delete it) plus a DNS
CNAME record `dgt.ggt.kr → kimshmath.github.io` at the domain registrar.
