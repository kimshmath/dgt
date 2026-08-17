# Dynamical Group Theory — conference series website

This repository hosts **https://dgt.ggt.kr** via GitHub Pages.

No build step — plain HTML/CSS. **Any push to `main` deploys automatically** within a
minute or two.

- [`index.html`](index.html) — the landing page: hero (with the Penrose P3 canvas
  animation) and the timeline of every edition. All CSS/JS inline.
- `dgt1/`, `dgt3/`, `dgt4/` — per-event pages for editions whose original websites went
  offline, rebuilt from the organizers' own records. They share [`event.css`](event.css).
- Editions with a live website of their own (II, V, VI, VII, VIII) link straight to it
  from the timeline instead of having a page here.

## How to add a page for an event

Copy `dgt4/index.html` to a new folder (e.g. `dgt9/index.html`) and edit the hero,
`Program`, `Organizers`, and `Sponsors` blocks. Keep `<link rel="stylesheet"
href="../event.css">` as is, then point that edition's timeline link at `dgt9/`
with the label `Details →`.

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
- For an event with no live website, build a page here (see below) and link it as
  `<a class="event-link" href="dgtN/">Details →</a>`.
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
