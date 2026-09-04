# 07 — Event/Organization Directory Listing Management

**Rank: ~7% of sampled inbound, medium-high reply-need.**

## What this category is

Questions and requests about WOWSA's public Directory: claiming a listing, adding a new listing (coach, organizer, event, association), or editing an existing one.

## Important: the Directory platform is mid-migration

WOWSA is retiring **Brilliant Directories (BD)**, the current legacy directory platform, in favor of a custom-built **canonical Person/Directory system** on Supabase + Lovable (project `wowsa-coach-finder`, "WOWSA Platform Main Production App"). This is a locked product strategy (locked 2026-08-26) but the build is in progress, not complete. **As of this writing, BD is very likely still the live platform customers actually interact with day to day** — don't assume the new system is live for a given feature without checking. When in doubt, check what `openwaterswimming.com`'s live Directory pages actually show.

The new architecture, once live, changes the model significantly: one canonical Person profile per individual (not a separate listing per role), discovered through Swimmer/Coach/Organizer lenses. If a customer describes a request that doesn't make sense under the old BD flat-listing model (e.g. "why do I have two different profiles"), that's likely a sign the new system is partially live for them, check `/people/<slug>` URLs directly.

**Gmail labels**: `SUPPORT/General Inquiries` for most directory questions; no dedicated directory label confirmed.

**Public docs**: `openwaterswimming.com/docs/` → "Claim Your Listing" category (Claim Your Listing, Find Your Listing) and "Add a Listing" category (How to Add a Listing [First Time Users], How to Add a Listing or Event [Registered Users], How to Edit Your Listing) and "Login and Register" category.

## Sub-issues in this folder

| File | Sub-issue |
|---|---|
| `01-claim-listing.md` | Claiming an existing listing |
| `02-add-new-listing.md` | Adding a new listing (coach/organizer/event/association) |
| `03-edit-existing-listing.md` | Editing/updating an existing listing |
| `04-event-race-listing-management.md` | Event/race-specific listing management |
