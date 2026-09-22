# yonder-monthly-reports

HTML snapshots of the unified monthly performance email, captured from local Mailtrap. Used to compare how the same template looks for different activity providers and plan states.

Product code lives in `yonder-api` (`MonthlyPerformanceAssembler`, `monthly_performance.blade.php`, `performance-email:send`). This repo does not send mail.

## How to view

Open `index.html` in a browser, or open a snapshot file directly.

## Current snapshots

| File | State | AP | Month |
| --- | --- | --- | --- |
| [no-results.html](no-results.html) | On plan, no results. Chatbot zeros, voice and reviews dashes, smart summaries empty state. | Infinity Applications (123) | August 2026 |
| [all-upsell.html](all-upsell.html) | Not on plan. Chatbot, Voice, and Reviews each show the spec upsell copy and Explore CTA. | Infinity Applications (123) | August 2026 |

## Adding a snapshot

1. Send a preview from yonder-api: `docker exec -it yonder-api php artisan performance-email:send --ap=<id>`
2. Copy the HTML from Mailtrap.
3. Save it as a new `.html` file here.
4. Add a row to `index.html` and `index.json`.
