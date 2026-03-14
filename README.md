# Run Weather Planner

Simple, beautiful tool to find optimal running windows based on weather conditions.

**Live:** https://run-weather.pages.dev  
**GitHub:** https://github.com/kaufmanhenry/run-weather

## Features
- 7-day forecast with hourly breakdowns
- Morning (6-9am) and evening (4-7pm) running windows
- Smart rating system based on:
  - Temperature (ideal: 40-55°F)
  - Feels-like temp (wind chill/heat index)
  - Precipitation probability
  - Wind speed
- Mobile-friendly, works offline after first load
- No API keys required (uses Open-Meteo)

## Rating System
- **Excellent** (80-100): Perfect conditions
- **Good** (60-79): Minor compromises
- **Fair** (40-59): Challenging but doable
- **Poor** (<40): Consider rescheduling

## Deploy
```bash
# Cloudflare Pages
wrangler pages deploy . --project-name=run-weather

# Or just open index.html locally
open index.html
```

## Built
March 14, 2026 — Nightly Build #1 (retroactive for Mar 13)
