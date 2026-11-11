# AAPL Options Expiration Tracker

> Weekly tracking of Apple (AAPL) option expirations for the risk review.
> All market figures below were pulled from **live Yahoo Finance data** on 2026-11-11.
> Share price used throughout: **$355.63** (AAPL regular market price, NasdaqGS, USD).

## 1. Company Snapshot (AAPL)

| Field | Value |
|---|---|
| Company | Apple Inc. |
| Ticker | AAPL (NasdaqGS, NMS) |
| Headquarters street address | **One Apple Park Way**, MS 927-4GC |
| City | **Cupertino** (state: CA, ZIP: 95014, United States) |
| Sector | **Technology** |
| Industry | **Consumer Electronics** |
| Current share price | **$355.63** (regularMarketPrice; post-market $355.47; previous close $348.51) |
| Market cap | ~$5.17T (non-diluted ~$5.06T) |
| Trailing P/E | 39.60 (forward P/E 33.70) |
| Analyst consensus | Buy (mean 2.22, 40 analysts; mean target $344.62) |
| CEOD resting on data | Kevan Parekh (Sr. VP & CFO); John Ternus (CEO & Director) |
| Employees | 167,000 full-time |
| Website | https://www.apple.com |
| Long name | Apple Inc. |

## 2. Expiration Map (available expirations, as returned by Yahoo Finance)

```
2026-11-11, 2026-11-13, 2026-11-16, 2026-11-18, 2026-11-20, 2026-11-27,
2026-12-04, 2026-12-11, 2026-12-18, 2026-12-24, 2027-01-15, 2027-02-19,
2027-03-19, 2027-04-16, 2027-06-17, 2027-09-17, 2027-12-17, 2028-01-21,
2028-03-17, 2028-06-16, 2028-12-15, 2029-01-19
```

**Three soonest upcoming expirations analyzed (today = 2026-11-11):**
1. **2026-11-11** (today)
2. **2026-11-13** (2 days out)
3. **2026-11-16** (5 days out)

*A note on repo naming: `aapl-expiration-tracker`, `aapl-expiration-tracker-2`, `-3`, `-4`, `-5`, `-7`, `-11`, and `-13` already existed in this GitHub org, so this tracking repo was created under the name `apple-op-expirations-tracker`.*

## 3. Per-Expiration Chain Stats

Share price used for ATM determination: **$355.63**

### Expiration 2026-11-11

| Metric | Value |
|---|---|
| ATM strike (closest to $355.63) | **355** |
| Highest-OI call strike | **355** (OOI 33,155; contract AAPL261111C00355000) |
| Highest-OI put strike | **347.5** (OOI 6,358; contract AAPL261111P00347500) |

 supported detail:
- Calls: 355 (OOI 33,155) > 352.5 (4,930) > 357.5 (8,464) > 350 (6,003) > 360 (19,451).
- Puts: 347.5 (6,358) > 340 (5,854) > 342.5 (4,727) > 350 (3,844) > 345 (3,921).
- Tight $2.50 strike grid near the money; heavy OI concentration at 355.

### Expiration 2026-11-13

| Metric | Value |
|---|---|
| ATM strike (closest to $355.63) | **355** |
| Highest-OI call strike | **360** (OOI 16,819; contract AAPL261113C00360000) |
| Highest-OI put strike | **330** (OOI 10,223; contract AAPL261113P00330000) |

 Supported detail:
- Calls: 360 (OOI 16,819) > 365 (11,856) > 355 (11,813) > 350 (7,547) > 357.5 (4,246).
- Puts: 330 (OOI 10,223) > 340 (9,560) > 322.5 (6,921) > 325 (6,779) > 320 (3,797).
- Coarser $5 strike grid at the money vs. the 2026-11-11 expiry; OI leaders differ by side (calls at 360, puts at 330).

### Expiration 2026-11-16

| Metric | Value |
|---|---|
| ATM strike (closest to $355.63) | **355** |
| Highest-OI call strike | **355** (OOI 5,737; contract AAPL261116C00355000) |
| Highest-OI put strike | **330** (OOI 1,537; contract AAPL261116P00330000) |

 Supported detail:
- Calls: 355 (OOI 5,737) > 350 (OOI 559) > 360 (OOI 801) > 340 (OOI 417).
- Puts: 330 (OOI 1,537) > 320 (OOI 951) > 340 (OOI 1,175) > 350 (OOI 359).
- Thin OI volume relative to at-the-money week (2026-11-11); only ~4 days to expiry.

## 4. TL;DR for the Risk Slide

| Expiry | ATM strike | Top call OI strike (OOI) | Top put OI strike (OOI) |
|---|---|---|---|
| 2026-11-11 | 355 | 355 (33,155) | 347.5 (6,358) |
| 2026-11-13 | 355 | 360 (16,819) | 330 (10,223) |
| 2026-11-16 | 355 | 355 (5,737) | 330 (1,537) |

- ** Booth/BID positioning:** OI concentration sits at 355 on both call and the 11-16 expiry; on 11-13 calls lean to 360 and puts to 330.
- **Data source:** Yahoo Finance (options chain + stock profile), pulled 2026-11-11.
- ** boxing:** this file lives on the `add-expirations-markdown` branch and is proposed via pull request into `main`.
