<p align="center"><img src="brand/logo.png" alt="Simply Budgets" width="420"></p>

Simply Budgets is a free budget app that runs on your phone. You track everything by hand, in a few quick ways, and nothing ever leaves your device. No bank logins, no accounts, no ads, no tracking.

**Use it:** https://laserjosh64.github.io/simply-budgets/

## Add it to your phone

- **iPhone:** open the link in Safari, tap Share, then Add to Home Screen.
- **Android:** open the link in Chrome and tap Install when the app offers it, or use the menu and tap Install app.

It then opens full screen from its own icon and works offline.

## The four tabs

- **Home:** spending money left, this month's categories (tap one to log a purchase), your goals, the Retirement card, and recent purchases.
- **Plan:** your paycheck, what's taken out of it, your categories, recurring bills, and student loans.
- **Activity:** everything you've logged as a list or by month, the bank file check, and spreadsheet downloads.
- **Accounts:** balances (checking, savings, emergency, card owed), goals, debts, and a savings projection.

## What it does

**Pay and deductions**
- Works from your take-home pay, or from your pay before deductions with taxes, Social Security, Medicare, 401(k), and anything else taken out first.
- **Retirement match:** mark which deductions go to retirement (401(k), pension, SERS and similar are picked out by name) and add your employer's match as a % of your contribution, a % of pay, or a set dollar amount.
- Drag deductions by their grip to put them in the order you like.

**Categories**
- Every category is yours to rename, recolor, give an icon or your own photo, or remove. Drag them to reorder; the same order shows on Home.
- Give each one a set amount or a share of what's left, with sliders that stop at 100%.
- Choose what happens to money left over at the end of the month: it rolls over (overspending carries too), or it moves to an account and is added to next month's amount for the saving category you pick.
- Presets: 50/30/20, pay yourself first, and even split, with Revert to undo.

**Logging spending**
- Type it in, or scan a receipt. The scan reads the store, each item and its price, and lets you put each item in its own category. Tax and fees are shared out by each category's part of the total. It learns your stores.
- Recurring bills and subscriptions, taken off the top of your paycheck or out of one category's budget (like Netflix out of Personal).
- A weekly check-in against a bank export file (CSV or OFX) to catch anything you missed.

**Balances, goals, and debt**
- Balances update themselves from what you log. Paydays add your paycheck to checking and roll to the next one. Credit card spending is tracked until you mark the card paid.
- Goals that read from your accounts and plan: save up, emergency cushion, pay off a debt, or keep a minimum. Goals can hold sub-goals and their own photo.
- Debt payoff with the snowball or avalanche method.
- **Student loans** sit in their own section of Plan with monthly interest added. They're kept out of the snowball and avalanche plan.
- **Retirement card** on Home: start from your latest statement balance, and each month's contributions and match are added. Tap it for a month-by-month list or to update the balance.

**Saving your work**
- Saved budgets, a 3-year savings projection, and CSV downloads (monthly totals or every purchase) that open in Excel, Google Sheets, or Numbers.

## Privacy

All data is stored in the app on your device. The app makes no requests to other sites; fonts and the receipt reader are bundled in this repo. See [privacy.html](privacy.html).

## Updating

After changing any file, run `python3 tools/make_sw.py` from the repository root, then commit and push everything, including the new `sw.js`. The script builds the version from the files' contents, so every change reaches installed phones. When the app finds a new version, it shows "A new version of Simply Budgets is ready" with an Update button. Saved data is kept.

## Credits

- Receipt reading: [Tesseract.js](https://github.com/naptha/tesseract.js), Apache License 2.0 (`vendor/tesseract`).
- Typeface: [Schibsted Grotesk](https://github.com/schibsted/schibsted-grotesk), SIL Open Font License 1.1 (`fonts/`).
