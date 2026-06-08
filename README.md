# SplitEase — Shared Expense Tracker

A Splitwise-style expense sharing app that runs entirely in the browser with no build step.

## How to run

Double-click `index.html` — that's it. No install, no server needed.
Requires an internet connection on first load (fetches React + Recharts from unpkg.com).

## Features

- **Folders** — group expenses by trip, household, office, etc. (create, edit name/icon/color, delete)
- **Members** — add/remove members per folder (≥ 2 required)
- **Expenses** — add, edit, delete; choose who paid and split equally or by custom amount
- **Balances** — see who owes whom with greedy debt simplification
- **Settle Up** — record a payment; suggested amounts are pre-filled
- **Analytics** — bar chart (paid vs. share per person), donut chart (by category), line chart (over time)
- **Delete folder** — only available when all balances are $0.00

## Assumptions / limitations

- **Persistence**: localStorage only — data is local to this browser. Clearing browser data removes everything.
- **No accounts / multi-device sync**.
- **Custom split** is by amount, not percentage.
- **Member removal** is blocked if the member has any expense or settlement reference — delete their expenses first.
- **Rounding**: equal splits are rounded to 2 decimal places; the rounding penny is assigned to the payer.
