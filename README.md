# Run Weather

An editorial almanac for the distance runner. Find the best training windows in the week ahead — at a glance.

**Live:** https://weather.setlist.run
**GitHub:** https://github.com/kaufmanhenry/run-weather

## Features

- **Runner-specific verdicts** — Perfect / Solid / Tough / Skip, not generic weather labels
- **"The Pick"** — the single best window of the week, answered up top
- **Morning + evening windows** per day (5–9am, 4–8pm)
- **Sunrise / sunset** on every day card
- **Dew point, wind, feels-like, rain** — the metrics runners actually use
- **7-day forecast**, past days filtered out
- **Remembers your last location** (localStorage)
- **No signup, no keys** — enter a city or zip

## Design

- **Analog-editorial** aesthetic on a warm paper palette
- **Fraunces** (display, numerics, rating words) paired with **Instrument Sans** (micro UI, labels)
- Hierarchy driven by type weight and hairline rules — no card chrome
- Italic serifs and small-caps sans for an almanac feel

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
- [Fraunces](https://fonts.google.com/specimen/Fraunces) + [Instrument Sans](https://fonts.google.com/specimen/Instrument+Sans) via Google Fonts
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

---

Built by [setlist.run](https://setlist.run).
