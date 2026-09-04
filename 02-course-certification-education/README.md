# 02 — Course / Certification / Education Questions

**Rank: #2 reply-needing category (~12% of sampled inbound).**

## What this category is

WOWSA runs two credential programs through **WOWSA Academy** (Kajabi): **Safe Coach Foundations** and **Safe Organizer Foundations**. Customers write in about enrollment, course access, progress, certificates, and pricing.

## System architecture (know this before answering anything here)

Three systems, each owns a specific piece, this division matters for knowing where to look:

- **Kajabi** (WOWSA Academy, site ID `2148882029`, `academy.openwaterswimming.com`) owns purchase/access, course delivery, and lesson/quiz completion events.
- **Airtable base "WOWSA Education & Credentials"** (`appm0S89Eu53KWqXc`) is authoritative for learner records, assessment evidence, and certification/credential issuance. **A second, duplicate-named base (`appKO1bHZsRv5cshC`) existed and was deleted 2026-08-30 — if you ever see it referenced anywhere, it's stale, the single correct base is `appm0S89Eu53KWqXc`.**
- **Lovable** (project `check-coach-standard`, workspace "Quinn's Lovable") renders the public credential/verification page, certificate, and feeds the Directory. Public sync endpoint: `https://www.openwaterswimming.com/api/public/credentials/sync`.

**Gmail label**: `SUPPORT/Coaching Certification`.

**Note**: WOWSA previously ran courses through a WordPress/LearnDash setup. There's a live page titled "Our courses are moving to a new platform" (`openwaterswimming.com/our-courses-are-moving-to-a-new-platform/`) — if a customer references an old course link or LearnDash-era course, they may need redirecting to the current Kajabi-based WOWSA Academy instead.

## Sub-issues in this folder

| File | Sub-issue |
|---|---|
| `01-certificate-not-received.md` | Completed the course but no certificate/credential issued — **known bug pattern, check this first** |
| `02-course-access-enrollment.md` | Can't access a purchased course, enrollment questions |
| `03-course-progress-status.md` | "How far am I / did my progress save" |
| `04-safe-coach-vs-safe-organizer.md` | Confusion between the two credential programs |
| `05-pricing-cohort-offers.md` | Pricing, current cohort offers, discounts |
| `06-old-platform-migration.md` | References to the old WordPress/LearnDash course platform |
| `07-refunds-cancellations.md` | Course refund/cancellation requests |
