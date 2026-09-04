# 06 — Billing, Payment, Subscription & Order Issues

**Rank: ~7% of sampled inbound, high reply-need (money issues need timely, accurate answers).**

## What this category is

Order confirmation, payment failures, refunds, subscription renewals/cancellations, and donation receipts.

## Where the data lives

- **WooCommerce** (via WordPress MCP) is the primary system for shop/e-commerce orders: `ewpa/wc-get-orders` (search/filter, HPOS-compatible), `ewpa/wc-get-order` (single order detail with line items and billing address), `ewpa/wc-get-customers` (customer + order stats), `ewpa/wc-update-order-status` (change status, add a note).
- **Kajabi** owns course-purchase-specific billing (see `02-course-certification-education/`), some of which may also route through WooCommerce depending on the product.
- An Airtable base **"Orders Sync to Airtable for WooCommerce Template"** (`appQy0dcByx3WNBwl`) exists but was last viewed 2026-02-22, likely stale/not actively maintained — prefer WooCommerce directly over this base unless told otherwise.

**Gmail labels**: `Billing` (top-level), `SUPPORT/Billing`, `SUPPORT/Payments`, `SUPPORT/Orders`, `SUPPORT/Donations`.

## Sub-issues in this folder

| File | Sub-issue |
|---|---|
| `01-order-not-received-confirmation.md` | "I paid but got no confirmation" |
| `02-refund-request.md` | General refund requests (non-course) |
| `03-subscription-renewal-cancellation.md` | Subscription/membership renewal or cancellation |
| `04-payment-failed-declined.md` | Payment failed or was declined |
| `05-donation-receipt-question.md` | Donation receipt / tax documentation requests |
