# Fee/payment questions tied to ratification

## What it is

Questions about ratification fees, usually embedded inside a status-check thread rather than standalone ("also, did our payment go through?").

## Where to check

- WooCommerce orders via WordPress: `ewpa/wc-get-orders` (search by customer email/name) — ratification fees are typically processed as WooCommerce orders.
- **Ratifications Pipeline** (`appgUjmgd0K8WWp31`) Notes field may reference payment status.
- Also see `06-billing-payment-orders/` for the general order/payment playbook, this file is specifically the ratification-fee flavor of it.

## How to answer

Confirm the specific order/payment status from WooCommerce rather than assuming from the ratification record alone, the two systems aren't always in sync.

## Escalate if

Payment shows as completed in WooCommerce but the ratification record shows unpaid/pending, or vice versa — that's a sync issue, flag to Rose rather than telling the customer to just resubmit.
