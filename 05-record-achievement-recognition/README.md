# 05 — Record/Achievement Recognition & Documentation

**Rank: ~8% of sampled inbound, medium reply-need.**

## What this category is

Questions and submissions related to the **WOWSA Awards** program and general record/achievement documentation (distinct from swim ratification itself, though the two are related — a swim usually needs to be ratified before an achievement/record claim about it is meaningful, see `01-ratification-swim-submission-status/05-record-first-claim-inquiries.md`).

## Where the data lives

**WOWSA Awards Archive** — base `appQIADxmbGpN8PbN` (most recently viewed of any awards-related base, 2026-09-01). Key tables:
- **Cycles** — one record per WOWSA Awards cycle/year.
- **Categories** — award categories per cycle (names have changed historically, preserved as-is).
- **Entities** — canonical people/teams/performances/events being recognized.
- **Award Records** — the central archive table, one record per nominee/finalist/winner per category per cycle.
- **Nominations** — incoming nomination submissions (nominee info, nominator info, achievement description).
- **Advisory Board** / **Board of Directors** — governance tables for who reviews nominations (note: internal-only fields like Email/Phone/Conflict Notes on these tables should never be shared externally).

**Gmail labels**: no dedicated `SUPPORT/Awards` label confirmed — check `SUPPORT/General Inquiries` and `SUPPORT/Stats/Reports`.

**Public reference**: site nav has a full "WOWSA Awards" section (Nominate, Categories, 1926-2026, History, Archive, Rules and FAQ, Governance, Partner, Press) — link customers to the specific relevant page rather than re-explaining program rules from scratch.

## Sub-issues in this folder

| File | Sub-issue |
|---|---|
| `01-awards-nomination-status.md` | Status of a submitted awards nomination |
| `02-record-claim-verification.md` | Verifying/documenting a record claim (cross-ref ratification) |
| `03-awards-archive-correction-request.md` | Requesting a correction to historical archive data |
