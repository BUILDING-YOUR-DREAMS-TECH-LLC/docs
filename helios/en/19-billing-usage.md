---
title: "Billing & Usage"
---

## Objective

Manage the subscription plan and monitor usage limits.

## Access

- Billing: /app/{tenant}/settings/billing
- Usage: /app/{tenant}/usage

## Roles

- owner, admin

## Billing

The page shows:

- Current plan (name, description, price).
- Subscription status.
- Features included.
- Usage meters (agents, users, documents, messages, etc.).
- Selector Plan for upgrade/downgrade.
- Customer Portal (Stripe).

Actions:

- Manage plan: open the plan selector.
- Customer Portal: manage payment, invoices and cancellation.

## Usage

- Shows consumption of the month and reset date.
- Includes limits of: Agents, Users, AI Messages, Documents.

## Good practices

- Check limits before enabling more channels.
- If you are close to the limit, consider upgrading.


## Screenshot

![Billing and Usage](../../images/helios/en/screenshots/billing-01-usage.png)

## Related

- [15-settings-general.md](./15-settings-general.md)
- [21-onboarding-plan.md](./21-onboarding-plan.md)

