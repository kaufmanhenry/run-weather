# Run Weather

Clean, runner-focused weather planner. Built for marathon training.

**Live:** https://run-weather.pages.dev  
**GitHub:** https://github.com/kaufmanhenry/run-weather

## Features

- **Runner-specific language** — Perfect/Solid/Tough/Skip (not generic weather ratings)
- **Smart windows** — Early morning (5-9am) and evening (4-8pm) sessions
- **Context-aware notes** — Ice risk, wind chill, heat warnings
- **7-day forecast** — Plan your week ahead
- **Mobile-first** — Check before heading out
- **No signup** — Just enter a city

## Design

- **Dark mode native** — Easy on the eyes at 5am
- **Strava-inspired** — Bold orange accent, clean hierarchy
- **Inter typeface** — Professional, readable
- **Data-first** — Temp/feels/rain/wind at a glance

## Rating System

**Perfect (85-100):** Ideal conditions  
**Solid (65-84):** Minor compromises  
**Tough (45-64):** Challenging but doable  
**Skip (<45):** Reschedule if possible

Scoring based on:
- Temperature (ideal: 40-55°F)
- Feels-like temp (wind chill/heat index)
- Precipitation probability
- Wind speed

## Tech

- Pure HTML/CSS/JS (no build)
- Open-Meteo API (free, no key)
- Inter font (Google Fonts)
- Deployable to Cloudflare Pages

## Deploy

```bash
cd ~/Code/run-weather
wrangler pages deploy . --project-name=run-weather --commit-dirty=true
```

---

**Built:** March 14, 2026  
**Nightly Build #1** (retroactive)
