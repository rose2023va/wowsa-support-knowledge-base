# 01 — Ratification / Swim Submission Status

**Rank: #1 reply-needing category (~13% of sampled inbound, highest of any category once low-reply press/marketing volume is excluded).**

## What this category is

WOWSA ratifies marathon/open water swims: a swimmer or their team submits a completed swim for official recognition, and WOWSA (or, for pre-approved partner associations, a co-ratification process) reviews the evidence and either ratifies it or asks for more. Most tickets in this category are a swimmer, coach, or association contact asking "what's the status of my/our submission."

## Where the data lives (read this before anything else)

**There are three Airtable bases with "Ratifications" in the name. Only one is current production. Do not guess from the name.**

| Base name | Base ID | Status |
|---|---|---|
| **Ratifications Pipeline** | `appgUjmgd0K8WWp31` | **Current production. Use this one.** Rose confirmed this as source of truth. Table "Workflow" tracks Swim ID, Swimmer's Name, Swim Date, Status, Notes, Ratification Page. |
| WOWSA Ratifications | `apppdxgNikq9FRbPp` | Next-generation rebuild, backend only, **not yet cut over**. Has a richer relational schema (Swims, Submissions, Ratifications, Decision Versions, Committee Votes, Evidence, People) but is not the live source of customer-facing status as of this writing. Do not tell a customer their status based on this base unless Rose has confirmed cutover happened. |
| Ratifications | `appy2Xm06RS845Q5L` | Legacy/unclear — do not use without checking with Rose first. |

Intake itself still runs through **Jotform** (the ratification submission form and the "Pre-approved Ratification" form for partner associations), not Airtable directly — Airtable is where status is tracked after intake.

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

**Write/consult guidance in this order**: status checks (#1) are both the most common and currently the most inconsistently handled (some same-day replies, others go months with repeated unanswered "gentle reminders" — this is the single highest-leverage fix available). Observer rules (#3) and pre-approval inquiries (#2) come next.
