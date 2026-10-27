<p align="center"><img src="brand/logo.png" alt="Simply Budgets" width="420"></p>

Simply Budgets is a free budget app that runs on your phone. You track everything by hand, in a few quick ways, and nothing ever leaves your device. No bank logins, no accounts, no ads, no tracking.

**Use it:** https://laserjosh64.github.io/simply-budgets/

## Add it to your phone

- **iPhone:** open the link in Safari, tap Share, then Add to Home Screen.
- **Android:** open the link in Chrome and tap Install when the app offers it, or use the menu and tap Install app.

It then opens full screen from its own icon and works offline.

## What it does

- Works from your take-home pay, or from your pay before deductions with taxes, Social Security, Medicare, 401(k), and anything else taken out first.
- Every category is yours to rename, recolor, give an icon, or remove. Give each one a set amount or a share of what’s left, with sliders that stop at 100%.
- Ways to log spending: type it in, scan a receipt (it reads the store and total on your phone and learns your stores), split one receipt across categories by highlighting the photo, or check a bank export file once a week to catch anything missed.
- Balances update themselves from what you log. Paydays add your paycheck to checking and roll to the next one.
- Goals that read from your accounts and plan: save up, emergency cushion, pay off a debt, or keep a minimum.
- Debt payoff with the snowball or avalanche method.
- Presets (50/30/20, pay yourself first, even split), rollover categories, saved budgets, a 3-year savings projection, and a month-by-month spreadsheet you can download.

## Privacy

All data is stored in the app on your device. The app makes no requests to other sites; fonts and the receipt reader are bundled in this repo. See [privacy.html](privacy.html).

## Updating

After changing any file, run `python3 tools/make_sw.py` from the repository root, then commit and push everything, including the new `sw.js`. The script builds the version from the files' contents, so every change reaches installed phones. When the app finds a new version, it shows "A new version of Simply Budgets is ready" with an Update button. Saved data is kept.

## Credits

- Receipt reading: [Tesseract.js](https://github.com/naptha/tesseract.js), Apache License 2.0 (`vendor/tesseract`).
- Typeface: [Schibsted Grotesk](https://github.com/schibsted/schibsted-grotesk), SIL Open Font License 1.1 (`fonts/`).
