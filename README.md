# Run Weather

An editorial almanac for the distance runner. Find the best training windows in the week ahead — at a glance.

**Live:** https://weather.setlist.run

## Features

- **Runner-specific verdicts** — Perfect / Solid / Tough / Skip, not generic weather labels
- **"The Pick"** — the single best window of the week, set as the page's headline
- **At a glance** — every morning and evening of the week in one ruled table, each linking to its day
- **Morning + evening windows** per day (5–9am, 4–8pm)
- **Sunrise / sunset** on every day card
- **Dew point, wind, feels-like, rain** — the metrics runners actually use
- **7-day forecast**, past days filtered out
- **Remembers your last location** (localStorage)
- **No signup, no keys** — enter a city or zip

## Design

- The suite's **Almanac** page pattern (see `SUITE.md` in the setlist repo): dateline masthead, the answer as the headline, Roman-numbered sections over hairlines
- **Archivo** at 75% width (headings, the pick, rating words), **Archivo** (body), **IBM Plex Mono** (temperatures and figures)
- Warm paper palette; hierarchy from type and hairline rules, no card chrome

## Rating System

**Perfect (85–100):** Ideal conditions
**Solid (65–84):** Minor compromises
**Tough (45–64):** Challenging but doable
**Skip (<45):** Reschedule if possible

Scoring inputs:
- Temperature (ideal: 40–55°F)
- Feels-like (wind chill / heat index)
- Precipitation probability
- Wind speed
- Dew point (humidity load)

## Tech

- Single-file HTML/CSS/JS — no build step, no framework
- [Open-Meteo](https://open-meteo.com) for forecast data (free, no key)
- [Archivo](https://fonts.google.com/specimen/Archivo) + [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) via Google Fonts
- Cloudflare Pages hosting

## Deploy

Auto-deploys on push to `master` via GitHub Actions (`.github/workflows/deploy.yml`).

Required repo secrets:
- `CLOUDFLARE_ACCOUNT_ID`
- `CLOUDFLARE_API_TOKEN` (scopes: Cloudflare Pages:Edit, Account:Read)

Manual deploy:

```bash
wrangler pages deploy . --project-name=run-weather
```

## Part of the setlist.run suite

A small press of running tools for the distance runner:

- **[Setlist](https://setlist.run)** — what you listened to, synced to your pace
- **[Training Load](https://training.setlist.run)** — are you ready for tomorrow's workout?
- **[Run Weather](https://weather.setlist.run)** — the best training windows in the week ahead · _you're here_
- **[Gradient](https://gradient.setlist.run)** — the grade profile of any Strava segment

---

Built by [setlist.run](https://setlist.run).
