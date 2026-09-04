# "I paid but got no confirmation"

## What it is

Customer believes they completed a purchase but never received an order confirmation email, or can't find their order.

## Where to check

`ewpa/wc-get-orders` filtered by customer email, or `ewpa/wc-get-customers` to find their account and order history. Confirm the order actually exists and its payment status before responding.

## How to answer

If the order exists and is paid: confirm the order number and details directly, and resend/describe the confirmation info yourself in case the original email didn't arrive (check spam as a possibility too).
If no matching order exists: don't assume it's lost, ask for the payment method/date/amount to help trace it, and check whether the charge might have failed silently (see `04-payment-failed-declined.md`).

## Escalate if

Customer has a bank/card statement showing a charge but no matching WooCommerce order exists at all, that's a real discrepancy, escalate rather than telling them to just try again (which could result in a double charge).
