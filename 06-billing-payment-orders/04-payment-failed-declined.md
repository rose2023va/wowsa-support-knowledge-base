# Payment failed or was declined

## What it is

Customer trying to complete a purchase and their payment isn't going through, or was told it declined.

## Where to check

`ewpa/wc-get-orders` to see if a failed-status order exists for them at all (a fully-failed payment sometimes doesn't create a visible order, so absence isn't conclusive).

## How to answer

Suggest standard troubleshooting (check card details, try a different payment method, check with their bank for a hold). Don't speculate about why a specific card was declined, that information isn't available to WOWSA.

## Escalate if

Repeated failures that seem to be on WOWSA's side (e.g. the checkout itself appears broken, not just one customer's card) — that's `10-technical-website-issues/`, not a one-off billing question.
