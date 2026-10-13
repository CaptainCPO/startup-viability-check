# Changelog

## v1.1 (2026-10-13)
- Research starts from the decision and a known / unknown / hypotheses ledger; the Evidence Pack lists sources tried and unavailable.
- Internal data map for businesses with customers (billing, CRM, ad accounts, analytics — owner, period, format, anonymisation).
- Screening asks about the market environment (regulation, advertising limits, licensing, payment, logistics) as a kill factor.
- Market values carry `region` and `period`; the model flags figures from another region or older than 24 months, the report shows the flag; library entries are checked against the case region.

## v1.0 (2026-09-30) — first public release
- Two-case model (team vs market) with bridge, tornado on the market ranges, loaded CAC, sustained break-even, capital-need waterfall, cash-out month.
- Four verdicts incl. "Not assessable" for category estimates; conditions and the team's kill criterion on page 1.
- Interactive HTML report + verified PDF from the same source; Excel workbook with formulas recalculated by LibreOffice and compared to Python.
- Benchmark library with provenance flags (verified / stale / derived); `lib_audit.py`, `check_env.py`, `number_audit.py`.
- Languages: English, Russian.
- Licence: CC BY-NC 4.0.
