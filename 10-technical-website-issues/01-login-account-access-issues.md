# Can't log in

## What it is

Customer can't log into their WOWSA account on the main site (not specific to a Kajabi course login, see `02-course-certification-education/02-course-access-enrollment.md` for that).

## Where to check

`openwaterswimming.com/docs/` → "Login and Register" category has the standard login/registration flow. `ewpa/get-users` can confirm the account exists (note: per past experience this ability doesn't reliably expose email without a role filter and can time out, don't rely on it alone for email lookups, `ewpa/wc-get-customers` is more reliable for that).

## How to answer

Confirm the account exists first. Walk through standard password-reset steps. If the account genuinely doesn't exist under the email they're using, they may have registered under a different address, ask.

## Escalate if

Account exists, password reset isn't working, and this looks like a genuine site bug rather than user error.
