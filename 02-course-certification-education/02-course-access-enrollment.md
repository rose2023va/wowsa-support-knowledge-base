# Course access / enrollment questions

## What it is

Customer can't get into a course they believe they purchased, or is asking how to enroll.

## Where to check

- **Kajabi** (WOWSA Academy, site `2148882029`): check the customer's purchase/offer status and enrollment directly.
- WooCommerce (`ewpa/wc-get-orders`, `ewpa/wc-get-customers`) if the purchase might have gone through the WordPress shop rather than a direct Kajabi offer, some products/bundles route through WooCommerce.
- Confirm which credential program (Safe Coach vs Safe Organizer) and which cohort/offer they purchased, pricing and access differ, see `05-pricing-cohort-offers.md`.

## How to answer

- Confirm purchase status first before troubleshooting login, a login issue and a "never actually purchased" issue look identical from the customer's side.
- If purchased but not enrolled, this is usually a Kajabi-side access grant issue, check the offer's product/enrollment settings.
- Give clear, numbered steps for logging into `academy.openwaterswimming.com`.

## Escalate if

Purchase is confirmed (payment went through) but no enrollment exists anywhere and re-triggering it isn't something you have access to fix directly.
