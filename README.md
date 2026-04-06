# Jaylon · Card Readings — Main Hub

Live at: **https://jaylon-jackson.github.io**

This is the central hub for all client reading pages. It holds the readings directory, the repo/file structure conventions, and the reading types reference.

---

## Repo Naming Convention

| Type | Pattern | Example |
|---|---|---|
| Ongoing client (all readings) | `[Name]-Readings` | `Natalie-Citadel-Readings` |
| Standalone week reading | `[Name]-Week-Ahead-[Month]-[Day]-[Year]` | `Armani-Week-Ahead-April-6-2026` |
| One-time reading | `[Name]-[Type]-[Year]` | `Dionna-s-Soul-Portrait` |
| This hub | `jaylon-jackson.github.io` | — |

---

## File Structure — Ongoing Client Repo

```
index.html                    ← always the current reading
deck-opener.jpg               ← static, reused every week (never replace unless decks change)
face-down.jpg                 ← current week spread, cards face down
face-up.jpg                   ← current week spread, cards revealed
archive/
  week-march-30-2026.html
  monthly-march-2026.html
```

---

## Weekly Workflow

When a new reading is ready:

1. Move current `index.html` → `archive/week-[date].html`
2. Replace `face-down.jpg` and `face-up.jpg` with this week's photos
3. New `index.html` goes in root — client URL stays the same, no new link needed
4. `deck-opener.jpg` stays untouched
5. Update the hub's readings directory with new date range and status

---

## HTML Standards (Applied to Every Reading Page)

- **Images as repo files** — never base64 in HTML. Target: HTML under 80 KB
- **Special characters as HTML entities** — `&mdash;` `&middot;` `&rsquo;` etc. (required for Safari)
- **Countdown timer + save instructions** — added near bottom of every reading
- **Expiry gate overlay** — week readings expire Sunday midnight ET, monthly readings expire 40 days out
- **Print CSS** — hides timer/save section so PDF stays clean
- **Deck opener** — static base64 embed is fine (small, one-time, never changes)

---

## Expiry Schedule

| Reading Type | Expires |
|---|---|
| Week Ahead | Sunday midnight ET (end of that week) |
| Monthly | 40 days from delivery date |
| Soul Portrait | No expiry (permanent page) |
| Annual | No expiry (permanent page) |

---

## Active Repos

| Repo | Type | Status |
|---|---|---|
| [Armani-Week-Ahead-April-6-2026](https://github.com/Jaylon-Jackson/Armani-Week-Ahead-April-6-2026) | Week Ahead | Active |
| [Natalie-Citadel-Readings](https://github.com/Jaylon-Jackson/Natalie-Citadel-Readings) | Ongoing client | Active |
| [Naomi-Citadel-Readings](https://github.com/Jaylon-Jackson/Naomi-Citadel-Readings) | Ongoing client | Active |
| [Tiffany-s-Soul-Portrait](https://github.com/Jaylon-Jackson/Tiffany-s-Soul-Portrait) | Soul Portrait | Archived |
| [Dionna-s-Soul-Portrait](https://github.com/Jaylon-Jackson/Dionna-s-Soul-Portrait) | Soul Portrait | Archived |
