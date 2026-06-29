# StaySignal

Hotel booking quality scorer — know before they cancel.

Enter four booking details and get an instant **Booking Quality Score** (0–100), plain-English risk drivers, and a recommended action. Powered by a machine learning model trained on 119,390 real hotel booking records.

**Live demo:** [staysignal.vercel.app](https://staysignal.vercel.app)

---

## What it does

Hotels lose revenue when bookings cancel at the last minute — leaving rooms empty with no time to resell. StaySignal reads four signals in a booking that predict whether a guest will actually show up, and tells you what to do about it before it's too late.

---

## The four predictors

| Input | Why it matters |
|-------|---------------|
| Booking channel | Online TA cancels at 36.7% vs Direct at 15.3% — a 2.4× gap |
| Lead time | 180+ day bookings cancel at 57% · 0–30 days cancel at 18.6% |
| Country of origin | Guest origin correlates with booking commitment patterns |
| Special requests | 0 requests = 47.7% cancel · 5 requests = 5.0% cancel |

---

## How it works

1. Enter the booking channel, lead time, guest country, and number of special requests
2. StaySignal scores the booking 0–100 in real time
3. See the top risk drivers in plain English
4. Get one recommended action — request a deposit, send an engagement email, or add to overbooking buffer

---

## Tech stack

- React + Vite + Tailwind CSS
- Axios for API calls
- Deployed on Vercel
- Backend: [staysignal-api](https://github.com/kwitykwity/staysignal-api) — FastAPI + XGBoost on Render

---

## Local development

```bash
npm install
npm run dev
```

Requires the StaySignal API running locally at `http://127.0.0.1:8000`.
See [staysignal-api](https://github.com/kwitykwity/staysignal-api) for backend setup.

---

## Data source

António, N., Almeida, A., & Nunes, L. (2019). Hotel booking demand datasets.
*Data in Brief*, Vol. 22, pp. 41–49.
Real PMS data · 119,390 booking records · 2015–2017

---

## Key findings

- **37%** of hotel bookings never became stays — 44,224 of 119,390 canceled
- **$4.5M** in estimated lost revenue across two Portuguese hotels over two years
- OTA cancellations now approaching **50%** (Cloudbeds, 2026)
- Direct bookings generate **$519/booking** vs **$320** via OTA (SiteMinder, 2025)

---

## Part of

**StaySignal** — Hospitality Demand Intelligence & Booking Quality Scorer
Built by Christina Ruiz, Schiffon Wise, Chris Wozniak · Pursuit AI Native Fellowship 2026