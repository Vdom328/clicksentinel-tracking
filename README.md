# ClickSentinel Tracking Script

Lightweight, dependency-free click tracking snippet used by [ClickSentinel](https://clicksentinel.click) —
a traffic quality & click-fraud detection platform. Published here so anyone embedding it (or auditing a
site that does) can read exactly what it does before trusting it.

## What it does

- Listens for clicks on tracked buttons/links and sends an event to your ClickSentinel account
- Collects a session id, scroll depth and basic interaction signals used for bot/fraud scoring
- Runs async, ~5KB, no external dependencies, no cookies beyond `sessionStorage`

## What it does *not* do

- No fingerprinting beyond what's needed for duplicate/velocity detection
- No third-party data sharing — events go straight to your own ClickSentinel account
- No blocking of page render

## Usage

```html
<script>var SITE_ID = 123;</script>
<script src="https://clicksentinel.click/tracking-script.js"></script>
```

`SITE_ID` is the ID of your site in your ClickSentinel dashboard. Get one free at
[clicksentinel.click](https://clicksentinel.click) (free plan, no credit card).

## Source vs. build

This repo contains the **readable source**. The minified build served in production is generated with
`terser` (variable mangling, dead code removal) — functionally identical, just harder to read.

## License

MIT — use it, fork it, audit it.
