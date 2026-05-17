# Cardly Card Data CDN

This repo hosts `cards.json` — the credit card library that powers Cardly. Every time the app launches, it fetches the latest data from this repo via GitHub Pages.

## How it works

- **URL:** `https://navidia-admin.github.io/Cardly-data/cards.json`
- **Update frequency:** Every quarter (4x per year)
- **No app update needed** — all users get the new rates on their next app launch

## Quarterly update process

### When to update
1–2 weeks before a quarter starts (e.g., mid-March for Q2)

### What to do
1. Research new rotating categories:
   - Visit [doctorof credit.com](https://doctorof credit.com) → search "Q2 2026 rotating"
   - Or [awardwallet.com](https://awardwallet.com/credit-cards/quarterly-bonus-categories/)
   - Cross-reference 2+ sources

2. Edit `cards.json`:
   - For each rotating card (Chase Freedom, Discover It, etc.):
     - Move `currentQuarter` → beginning of `historical[]`
     - Add new `currentQuarter` with updated categories + rates + activation deadline
   - Update top-level `currentQuarter.label` and `endDate`

3. Commit & push:
   ```bash
   git add cards.json
   git commit -m "Update Q2 2026 rotating categories"
   git push
   ```

4. **Done.** All users see the update on their next app open.

## Schema

See [Cardly/CARDS_DATA_CDN.md](https://github.com/Navidia-Admin/Cardly/blob/main/CARDS_DATA_CDN.md) for the full schema and validation rules.

## Current quarter

- **Label:** Q2 2026
- **End date:** 2026-06-30
- **Last updated:** 2026-05-17
