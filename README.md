# WOWSA Support Knowledge Base

Internal knowledge base for WOWSA customer support, built to train a support-agent-facing AI chatbot from zero knowledge. Read `SYSTEM-INSTRUCTIONS.md` first if you are that AI.

## Contact driver ranking

Method: sampled deep-dive of `contact@openwaterswimming.com`, 283 genuine inbound threads reviewed (excludes pure automated notifications), January 2025 through September 2026, heaviest density in the trailing 13 months. Cross-checked against the live Gmail `SUPPORT/*` label taxonomy and WOWSA's public docs site structure. This is a representative sample, not an exhaustive lifetime count — revisit and re-sample periodically.

| # | Folder | Contact driver | ~Share of inbound | Reply-need |
|---|---|---|---|---|
| 1 | [`01-ratification-swim-submission-status`](01-ratification-swim-submission-status/) | Ratification / swim submission status | ~13% | High — top reply-needing category |
| 2 | [`02-course-certification-education`](02-course-certification-education/) | Course / certification / education questions | ~12% | High |
| 3 | [`03-press-media-inquiries`](03-press-media-inquiries/) | Press/media inquiries & partner press releases | ~20% (largest by volume) | Low — mostly one-way FYI |
| 4 | [`04-partnership-sponsorship-marketing`](04-partnership-sponsorship-marketing/) | Partnership, sponsorship & marketing outreach | ~12% | Low-medium |
| 5 | [`05-record-achievement-recognition`](05-record-achievement-recognition/) | Record/achievement recognition & documentation | ~8% | Medium |
| 6 | [`06-billing-payment-orders`](06-billing-payment-orders/) | Billing, payment, subscription & order issues | ~7% | High |
| 7 | [`07-directory-event-listing-management`](07-directory-event-listing-management/) | Event/organization directory listing management | ~7% | Medium-high |
| 8 | [`08-regional-federation-affiliate`](08-regional-federation-affiliate/) | Regional federation/affiliate correspondence | ~7% | Medium |
| 9 | [`09-general-open-water-membership`](09-general-open-water-membership/) | General open water swimming/membership questions | ~5% | Medium |
| 10 | [`10-technical-website-issues`](10-technical-website-issues/) | Technical/website issues | ~4% | High when it happens |

**Next in line** (identified, not yet fully built out — see [`11-next-in-line`](11-next-in-line/)):
- Openwaterpedia/content correction requests (~1%)
- Complaints, disputes & legal-adjacent requests (~1%, escalate-only, never auto-draft)
- Safer Together community program inquiries (newly identified during this build — high raw volume of automated interest-form intake, occasional real questions)
- New Registration / account access issues (automated welcome-email volume is huge; genuine "I can't log in" tickets are a real but smaller subset)

## How to add a new issue file

1. Confirm the pattern recurs (not a one-off) by checking the relevant `SUPPORT/*` Gmail label for volume.
2. Copy the template below into a new `.md` file in the right folder.
3. Fill in every section. Leave "Where to check" pointing at a specific, named tool/base/URL, never a vague "check Airtable."
4. Strip any real customer names, emails, or ticket-specific details before saving. This repo is private but is written as if public.

```markdown
# [Issue title]

## What it is

## How to recognize it

## Where to check

## How to answer

## Escalate if
```
