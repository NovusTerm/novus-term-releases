# Where every number in `README.md` comes from

⚠️ **NOTHING CHECKS THIS FILE OR THE README. There is no CI here, no facts test, no
drift guard.** The product repository has two automated guards that compare its public
claims against the code (`scripts/landingFacts.test.ts` and `scripts/privacyFacts.test.ts`),
and **neither of them can see this repository.** That is precisely how the page came to
advertise a macOS floor three versions too low, a trial three times too short and prices
roughly half the real ones, for **seventy-three days**, without anyone noticing.

So: **this page is checked by hand, by whoever changes the numbers it talks about.** This
file exists to make that thirty seconds instead of an afternoon.

## The table

Every claim, and the one place that decides it. Paths are in
`NovusTerm/novus-term-desktop`.

| Claim in `README.md` | Value today | Decided by |
|---|---|---|
| macOS floor (badge **and** Requirements — two places) | **14.0** | `src-tauri/tauri.conf.json` → `minimumSystemVersion` |
| Trial length | **21 days** | `src-tauri/src/licensing/config/windows.rs` → `TRIAL_DAYS` |
| Free history window | **30 days** | same file → `FREE_RETENTION_DAYS` |
| Prices, discounts, Macs per plan | **$9.99 / $26.99 / $95, two Macs on all three** | `src-tauri/src/licensing/config.rs` → `PLANS` |
| Free caps (terminal tabs, workspaces, …) | **20 tabs · 3 workspaces · panes uncapped** | `src-tauri/src/licensing/config.rs` → `CAP_*` |
| Which features are marked **Pro** | the 26 keys | `src-tauri/src/licensing/config.rs` → `PRO_FEATURES` |
| Theme count | **92** | `docs/landing-facts.json` → `themes.total` |
| Font count | **31** | `src/lib/fonts.ts` → `FONT_SEEDS` |

`docs/landing-facts.json` in the product repository is regenerated from the code on every
CI run, so it is the cheapest place to read most of these — **but never edit it by hand**,
and never copy a number out of it that the table above says lives elsewhere.

## Two rules that are not obvious

1. **A feature that stops being Pro must be removed from the Pro markers here.** The page
   spent two months selling floating panes and file search as Pro after both became Free.
   Selling somebody something they already have is the worst kind of error on this page:
   it is not a typo, it is a false offer at the moment of purchase.
2. ⚠️ **Never write that any tier is free "forever".** Owner's decision of 2026-08-16. The
   word closes off every later adjustment and reads as a broken promise the first time
   anything moves.

## When this stops being necessary

When a guard in the product repository fetches this README and compares it against
`docs/landing-facts.json`, the same way the website is compared today. Until then, the hand
check is the only thing there is — and the audit that produced this file recorded that a
real guard for a third repository is worth building **after** publication, when there is
something to protect.
