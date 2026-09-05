# Pre-approved ratification (partner association)

## What it is

A **separate process** from standard WOWSA ratification. A partner association or federation submits a swim that **the association itself already ratified under its own authority**, and WOWSA recognizes/co-ratifies it and issues a certificate. Submitted through the dedicated **"2025 WOWSA Pre-approved Ratification" Jotform**, which has a "Name of Association / Partner" field.

Associations seen using it: **LPSA** (Brazil), **Swim Oresund**, **OWAAF India**, and others including a Lagoa de Cima series.

## The mistake to avoid

**These swims do NOT appear in the Ratifications Pipeline Workflow table (`appgUjmgd0K8WWp31` / `tblulYhWIpP0E3eov`), and that is correct behavior, not a lost submission.** That table tracks the standard individual-swimmer pipeline only.

If you search Workflow for a pre-approved swimmer, find nothing, and conclude the submission was lost, you will alarm a partner association over a non-problem and damage a relationship WOWSA depends on. Confirm which process you are in before searching.

## How to recognize it

Any one of these is enough:
- Sender is an association or federation contact rather than the swimmer.
- Subject or body references "Pre-approved Ratification" or "WOWSA Pre-approved Ratification".
- Thread carries the `SUPPORT/Pre-Approved Ratifications` label (or a child like `.../Lagoa de Cima`), or `SUPPORT/LPSA`.
- The Jotform notification shows a populated "Name of Association / Partner" field.
- The association states the swim is already ratified on their side and they want WOWSA recognition or a certificate.

## Where to check

**Honest status: the tracking location is UNCONFIRMED. Ask Rose before quoting any status.**

Ruled out by direct inspection (2026-09-05):
- `appgUjmgd0K8WWp31` Ratifications Pipeline — 3 tables only (Workflow = standard pipeline, Table 1 = automation-only WooCommerce order intake and must not be hand-edited, Pre-Swim Planning). No pre-approved tracker.
- `appy2Xm06RS845Q5L` "Ratifications" — 5 records overlapping Workflow, appears to be a partial legacy duplicate.
- `apppdxgNikq9FRbPp` WOWSA Ratifications rebuild — full schema, zero records, not in production.

What does exist and is usable today:
- The **Jotform submissions** themselves, and their notification emails in Gmail.
- **Gmail labels** `SUPPORT/Pre-Approved Ratifications` and `SUPPORT/LPSA` — searching these is currently the most reliable way to reconstruct a case history.
- **Google Drive** folders holding evidence for some cases.
- **WooCommerce** if the association paid a fee, searchable by the payer's email.

## How to answer

- Confirm receipt with specifics (swimmer name, swim date, association) so the association knows the submission is not lost.
- Do **not** state a pipeline status from the Workflow table, it does not apply to this process.
- If they are chasing after a long silence, acknowledge the delay plainly. Several of these threads have gone months with repeated unanswered follow-ups, which is a relationship risk, not just a service delay.
- For certificate requests specifically: confirm what was received and what is still needed, then route to whoever issues pre-approved certificates.

## Escalate if

- The association has followed up more than once with no reply. Treat as priority, not routine.
- You cannot determine the case's status because the tracking location is unconfirmed. Route to Rose rather than guessing or implying it was lost.
- Payment was made but no certificate issued, cross-check WooCommerce and flag as a money issue.

## Related

- `08-regional-federation-affiliate/01-partner-association-ratification-coordination.md` — the relationship-management side of the same associations.
- Public wording rule: "Ratified by [Association] · Administered using WOWSA Ratification Infrastructure". Never imply WOWSA independently ratified a partner-association swim.
