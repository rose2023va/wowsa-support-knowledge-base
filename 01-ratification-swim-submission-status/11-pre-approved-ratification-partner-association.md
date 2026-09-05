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

## The process (confirmed by Rose, 2026-09-05)

**Two steps, in this order:**
1. **Pay via WooCommerce first.**
2. **Then submit the "2025 WOWSA Pre-approved Ratification" Jotform.**

That is the entire intake. **There is no Airtable tracking for pre-approved ratifications and no status field anywhere.** This is confirmed, not a gap someone still needs to find. Do not go hunting for a base; there isn't one.

Already ruled out by direct inspection so nobody re-searches them: `appgUjmgd0K8WWp31` (Workflow is the standard pipeline only; Table 1 is automation-only Woo order intake and must never be hand-edited; Pre-Swim Planning), `appy2Xm06RS845Q5L` (5 records, partial legacy duplicate), `apppdxgNikq9FRbPp` (schema only, zero records).

## Where to check, in order

Reconstruct the case from these three. No single place shows status.

1. **WooCommerce, did they pay?** This is step 1 of the process, so confirm it first. Use `ewpa/wc-get-customers` on the payer's email, then `ewpa/wc-get-orders` for that customer ID. Order status `processing` or `completed` means paid; `failed` means it did not go through.
   - **The product is "Association Pre-Approved Swim Ratification - Solo", `product_id 89580`, $30 USD.** That is how you identify a pre-approved order.
   - **The payer is usually NOT the swimmer.** Searching the swimmer's name often returns nothing even when the swim is fully paid for. Search the association's email, and be aware associations bill under staff names and secondary addresses (Swim Oresund bills as "Dennis Holm" across two emails; OWAAF bills as "Rahul chiplunkar" as well as its main address).
   - Known association customer IDs: Swim Oresund `17120`, LPSA `375`, OWAAF India `23201`.
2. **Gmail, did they submit the form?** Search labels `SUPPORT/Pre-Approved Ratifications` (child labels exist, e.g. `.../Lagoa de Cima`) and `SUPPORT/LPSA`. The Jotform notification from `noreply@jotform.com` with "2025 WOWSA Pre-approved Ratification" in the subject **is** the submission record, carrying association name, swimmer name, swim date and contacts.
3. **Google Drive** for evidence folders on some cases.

## Determining status when there is no status field

You infer it from the two steps:
- **Paid, no Jotform submission found** → waiting on the association. Chase them.
- **Paid and form submitted, no certificate issued** → waiting on WOWSA. This is where almost every complaint comes from.
- **Form submitted, no payment found** → check whether that partner pays in batches or was invoiced separately before saying anything.

## Order status cannot tell you whether it was delivered

**Paid orders sit in `processing` and are essentially never moved to `completed`.** Across 30 pre-approved orders inspected on 2026-09-05, `date_completed` was null on all of them. So a delivered ratification and a forgotten one look identical in WooCommerce.

Practical consequence: you cannot answer "have we delivered this?" from any system. You have to read the Gmail thread. Assume nothing from order status beyond "they paid."

## Why these rot, worth flagging upward

With no status field and no meaningful order status, a paid and submitted pre-approved case is invisible until the association complains. No queue, no aging view, nothing surfacing "paid, submitted, never delivered."

This matters more than it looks, because these associations are WOWSA's most repeat-purchasing customers. As of 2026-09-05: Swim Oresund 24 orders/$882, LPSA 26 orders/$989, OWAAF India 13 orders/$500. All three were simultaneously chasing undelivered work, one of them escalating by cc'ing Quinn. It is a process gap, not an individual failure, and it will keep recurring until something tracks state.

Cheapest available fix with existing tools: mark these orders `completed` when the certificate ships. That alone turns a WooCommerce filter on product 89580 into a working delivery queue.

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
