# 10 — Technical/Website Issues

**Rank: ~4% of sampled inbound, but high reply-need when it happens (broken functionality blocks whatever else the customer was trying to do).**

## What this category is

Bug reports, broken pages/forms, login problems not tied to a specific account issue, and general "the website isn't working" reports.

**Gmail label**: `SUPPORT/WordPress`, `SUPPORT/Jotform`, `SUPPORT/Forms`.

## Where the data/tools live

WOWSA's site runs on **WordPress** (page builder WPBakery, SEO plugin Yoast, LMS LearnDash legacy + Kajabi current, WooCommerce + Subscriptions/Memberships, PeepSo social, Wilcity directory theme). The `mcp__wowsa-wordpress__*` tools give direct access: `ewpa/get-posts`/`get-pages`/`get-cpt-items` for content, `ewpa/site-stats` and `ewpa/get-active-plugins` for a quick system health check, `ewpa/get-environment-info` for PHP/database/WordPress version diagnostics.

## Sub-issues in this folder

| File | Sub-issue |
|---|---|
| `01-login-account-access-issues.md` | Can't log in (general, not tied to a specific purchase) |
| `02-website-bug-reports.md` | General bug/broken-page reports |
| `03-form-submission-issues.md` | Jotform/website form not submitting or not received |
