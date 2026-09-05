# 01 — Ratification / Swim Submission Status

**Rank: #1 reply-needing category (~13% of sampled inbound, highest of any category once low-reply press/marketing volume is excluded).**

## What this category is

WOWSA ratifies marathon/open water swims: a swimmer or their team submits a completed swim for official recognition, WOWSA reviews the evidence, and a committee either ratifies it or asks for more. Most tickets in this category are a swimmer or their crew asking "what's the status of my submission."

## Three different things with confusingly similar names. Do not mix them up.

1. **Standard WOWSA ratification** — an individual swimmer submits their own swim. Gets a `SWIM-####` ID and runs the full pipeline. **This folder covers it.** Tracked in the Workflow table described below.
2. **Pre-swim planning / pre-approval inquiry** — a swimmer asking what they must do *before* attempting a swim so it qualifies. This is the front end of process 1, not a separate process. See `02-pre-approval-procedure-inquiry.md`.
3. **Pre-approved ratification** — a **partner association** (LPSA, Swim Oresund, OWAAF India and others) submits an already-completed swim that the association ratified under its own authority, through the separate "2025 WOWSA Pre-approved Ratification" Jotform. **This is a different process and is NOT tracked in the Workflow table.** Its absence from that table is normal, not a lost submission. See `11-pre-approved-ratification-partner-association.md`.

## Where the data lives (read this before anything else)

**There are three Airtable bases with "Ratifications" in the name. Only one is current production. Do not guess from the name.**

| Base name | Base ID | Status |
|---|---|---|
| **Ratifications Pipeline** | `appgUjmgd0K8WWp31` | **Current production. Use this one.** Rose confirmed this as source of truth. Table "Workflow" tracks Swim ID, Swimmer's Name, Swim Date, Status, Notes, Ratification Page. |
| WOWSA Ratifications | `apppdxgNikq9FRbPp` | Next-generation rebuild, backend only, **not yet cut over**. Has a richer relational schema (Swims, Submissions, Ratifications, Decision Versions, Committee Votes, Evidence, People) but is not the live source of customer-facing status as of this writing. Do not tell a customer their status based on this base unless Rose has confirmed cutover happened. |
| Ratifications | `appy2Xm06RS845Q5L` | Legacy/unclear — do not use without checking with Rose first. |

Intake runs through **Jotform**, not Airtable directly. Airtable is where status is tracked after intake, **but only for the standard pipeline.** The "2025 WOWSA Pre-approved Ratification" Jotform is a separate form feeding a separate process whose tracking location is currently unconfirmed, see `11-pre-approved-ratification-partner-association.md`.

**Gmail labels**: `SUPPORT/Ratifications` (parent label, plus many per-swim child labels like `SUPPORT/Ratifications/SWIM-1033`), `SUPPORT/Pre-Approved Ratifications`, `SUPPORT/Swimmer Ratification`, `SUPPORT/Jotform`. If a thread already has a `SUPPORT/Ratifications/SWIM-####` label, that SWIM ID is your fastest path to the Airtable record — search the Workflow table by Swim ID directly.

**Public reference docs** (link customers here for process questions): `openwaterswimming.com/docs/` → "Independent Marathon Swim Ratification" category (9 articles: GPS device guidance, observer roles, documentation standards, ratification procedures). Also `openwaterswimming.com/contact-wowsa/` → "Swim Ratification Documentation Reference" and "WOWSA Observer Log Template" under Help/Support.

## Sub-issues in this folder

Ranked by volume from a ~65-70 thread deep-dive sample of ratification-specific threads (Jan 2025-Sep 2026, heaviest in the trailing 4 months):

| File | Sub-issue | Volume |
|---|---|---|
| `01-status-check-follow-up.md` | Status check / progress follow-up | Highest (14-16 of ~65-70) |
| `02-pre-approval-procedure-inquiry.md` | Pre-approval / pre-swim procedure inquiry | 10-11 |
| `03-independent-observer-paperwork.md` | Independent Observer paperwork/rules | 7 |
| `04-post-swim-evidence-submission.md` | Post-swim evidence/documentation submission | 5-6 |
| `05-record-first-claim-inquiries.md` | Record/first-claim inquiries | 5 |
| `06-route-logistics-amendment.md` | Route/logistics amendment mid-swim | 4-5 |
| `07-rules-criteria-clarification.md` | Rules/criteria clarification (general) | 4 |
| `08-fee-payment-questions.md` | Fee/payment questions tied to ratification | 3-4 |
| `09-dispute-correction-of-decision.md` | Dispute/correction of a ratification decision | 3 |
| `10-governance-committee-threads.md` | Governance/committee threads | 2-3, mostly internal, likely out of scope for support |
| `11-pre-approved-ratification-partner-association.md` | **Pre-approved ratification (separate process)** | Read this before searching the Workflow table for any association-submitted swim |

**Write/consult guidance in this order**: status checks (#1) are both the most common and currently the most inconsistently handled (some same-day replies, others go months with repeated unanswered "gentle reminders" — this is the single highest-leverage fix available). Observer rules (#3) and pre-approval inquiries (#2) come next.
