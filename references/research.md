# Research checklist

Run searches in this order. Stop a line of search when you have two independent sources or have clearly exhausted it — don't chase a fifth source for a number that already agrees.

## 0. The decision first, then the ledger

Research serves one decision the founder has to make — name it before the first search: *invest the next three months or not · raise a round or bootstrap · enter this country / segment or another · raise the price or not*. A search that does not change that decision is not run. Then write the ledger in three lists and keep it in the Evidence Pack:

- **Known** — facts with a source (the founder's measured numbers, published prices, a regulator's rule).
- **Unknown** — what the decision needs and nobody has (a churn figure, a close rate, a licence requirement).
- **Hypotheses** — what the founder or the analyst believes, written as a checkable statement with the number that would confirm or refute it.

Each unknown gets a search or a measurement; each hypothesis gets the data that would settle it and where it comes from. The ledger is what the report's `conditions` and "next 90 days" are later written from, so unknowns that cannot be closed by research are already the first tests.

**For a live business, inventory the internal data before searching outside** (`references/intake.md` § Internal data map): the founder's own billing, CRM and ad accounts answer churn, conversion and acquisition cost more reliably than any benchmark.

## 1. Market

- Size of the addressable segment (not the headline TAM — the segment the Case Card names). Prefer bottom-up: number of target customers × realistic price.
- Growth direction and why (regulation, tech shift, buyer behaviour).
- Any recent funding rounds in the space — they reveal what investors believe and what prices/metrics are being achieved.

## 2. Competitors — three layers, all mandatory

### Direct
Same problem, same approach. For each (2–4):
- Name, URL, pricing (actual numbers), target customer
- **Any published operating figure**: take rate or commission, free→paid conversion, reported customer count, churn or retention, funding and headcount. These feed the market column of the Assumptions Pack (`calibration.md`); capture the exact figure, the page, the date, and the currency.
- What users praise / complain about (G2, Capterra, Reddit, Product Hunt comments, app-store reviews)
- Funding / team size if public — signals how hard they can push

### Indirect
Same problem, different approach. Think: consultants and agencies, templates and courses, spreadsheets and manual processes, in-house tools, "do nothing". For each (2–4):
- What it costs the buyer (money and time)
- Why a buyer picks it over a product like this one

This layer tells you the real price anchor and the real switching cost.

### Displacers
Not competing today, but could remove the need for the product. Always check:
- General-purpose AI (ChatGPT, Claude, Gemini, Copilot) — can a motivated user get 70% of the value with a good prompt?
- Platform features — is the incumbent platform (Shopify, HubSpot, Notion, Salesforce, the app store owner…) likely to ship this natively?
- Behaviour shift — is the underlying need shrinking?

For each displacer, write one line: **Defence:** what stops it (data moat, workflow lock-in, regulation, distribution, trust) — or "none identified".

## 3a. Library first, then refresh

Start from `references/benchmarks.json`: list the entries that apply to this case's motion, type and segment. For each, try to find a fresher or higher-tier source (primary > survey > secondary). Add what you find as new entries in the Evidence Pack with the same fields (domain, value, tier, source, date, n) — never overwrite the library in place. Entries older than 24 months must be refreshed or flagged stale.

## 3b. Growth benchmarks for the motion

Take the motion from the Case Card and pull the funnel benchmarks listed for it in `growth.md` (Axis 1), refined for this segment: CPC/CPL for the vertical, landing/signup CR, trial→paid, meetings per rep, demo→close, sales cycle, partner listing CTR, k-factor. Each becomes one row of the funnel table with its source.

## 3c. Comparable benchmark (reference)

- `segment_size`: count of target customers (companies or people), not a dollar TAM. Bottom-up from the customer definition in the Case Card.
- `comparable_penetration`: share of that segment reached by 2–3 comparable products after ~3 years (their reported customer counts ÷ segment). If none found, note it; the model will use 1–3 % marked speculative. This is a reference for the plausibility of the funnel, not a ceiling.
- For a paid motion, also pull CPC/CPL for the vertical so the budget → customers funnel can be built; CAC will be derived from it.

## 3d. Unit-economics benchmarks for the business type

Take the type from Axis 2 in `growth.md` and confirm its ranges for this segment:
- Cost to acquire a customer by channel (paid social, search, outbound, partnerships, self-serve)
- Monthly churn (convert annual retention: `monthly_churn = (1 − annual_retention^(1/12)) × 100`)
- Gross margin typical for the archetype
- Free-to-paid or trial conversion
- Net revenue retention / expansion
- Sales cycle length for the segment

Good sources: OpenView / Bessemer / a16z / ChartMogul / ProfitWell / Lenny's Newsletter benchmark posts, SaaS Capital surveys, public S-1 filings of comparable companies, industry-specific reports. Tag each as `benchmark` or `proxy` depending on how close the archetype match is.

## 4. Risks outside the model

- Regulation or compliance affecting the segment (GDPR, HIPAA, financial licensing, AI-specific rules); for a new country or vertical also advertising restrictions, licensing or certification, accepted payment methods, logistics and tax — anything that can forbid or price out the sale before the economics matter
- Platform dependency (API terms, app-store policy)
- Concentration — does the business depend on one channel or one partner?

## Evidence Pack format

```
| # | Claim | Value | Source | Quality | Region · period |
|---|-------|-------|--------|---------|-----------------|
| 1 | Paid-social CAC, B2B SaaS SMB | $300–600 | https://… | benchmark | US · 2025 |
| 2 | Competitor X price | $49/seat/mo | https://… | direct | EU · 2026-03 |
```

Every claim carries the region and the period the figure describes; a figure from another region or older than two years is still usable, but the mismatch is written next to it and the model's `region` / `period` fields on the market value carry it into the report. Then the three competitor tables, a short "Risks outside the model" list, and **"Sources tried and unavailable"** — pages that did not load, reports behind paywalls, datasets that exist but were not reached — so the next pass knows what to try and the reader knows what the pack does not rest on. No narrative.


## When the company's own site cannot be read

Sites behind bot protection or client-side rendering return an empty fetch. Do not stop and do not guess: read the company from (1) independent reviews and comparison pages (rivals' blogs are useful for prices and offers but are biased on quality — cite them as `secondary` and never as the only source for a positioning claim), (2) the founder's LinkedIn page and posts, (3) Product Hunt / G2 / Trustpilot listings, (4) the Wayback Machine snapshot of the site, (5) a 30-minute call with the founder — which for a live business is also the only way to get the measured numbers. Every figure taken this way carries the page it came from and the date; a price seen only in a rival's review is `founder_stated` at best, not `observed`.
