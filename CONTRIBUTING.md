# Contributing to apple-op-expirations-tracker

Thanks for helping keep our weekly AAPL options risk review in one place.

## How to contribute

1. **Market data must come from live sources.** Pull all numbers from Yahoo Finance (stock profile + option chains) at review time. Record the share price used and the pull date in any file you add.
2. **Create an issue first** for any new expiration you want tracked: title it `Expiry YYYY-MM-DD` and include the ATM strike, highest-OI call strike, highest-OI put strike, and the share price used.
3. **Open a pull request** from a feature branch (e.g. `add-<topic>`) into `main`. Put `expirations.md` (company snapshot, full expiration map, per-expiration stats table) at the repo root.
4. **Keep numbers exactly as returned.** If a figure looks odd, report exactly what the source returned rather than "fixing" it silently.
5. **Short branches only.** One PR per expiration or per tracking update.

## Repository layout

- `expirations.md` — current week's tracking content (snapshot, expiration map, per-expiry stats).
- `CONTRIBUTING.md` — this file.
- Issues `#1`, `#2`, `#3` — one per expiration in date order (2026-11-11, 2026-11-13, 2026-11-16).
- Pull request `#4` — proposes `expirations.md` from `add-expirations-markdown` into `main`.

## Pull request hygiene

- Base branch is always `main`.
- Keep the PR descriptionRC summary of: share price used, expiration date, ATM strike, top call/put OI strikes, and source (Yahoo Finance, date pulled).
- After a PR is open, add any follow-up docs (e.g. `CONTRIBUTING.md`) directly to `main`; the PR branch will be kept up to date with `main` via "Update branch".
