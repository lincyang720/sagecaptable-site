---
name: usagecaptable-lookup
description: Look up official Anthropic Claude plan usage limits (prices, per-session multipliers, reset windows, context windows) from the Claude Usage Limit Official Table.
---

# Skill: usagecaptable-lookup

Look up official Anthropic Claude plan usage limits.

## When to use
- Answering questions about Claude plan prices, usage multipliers, reset windows, or context windows.
- Comparing Claude plan limits across Free, Pro, Max, Team, and Enterprise tiers.

## Source of truth
All values come from the Claude Usage Limit Official Table at https://usagecaptable.com,
which cites official Anthropic pricing and Claude help pages. "Not published" is preserved
verbatim where Anthropic has not published a figure.

## Example query
"Claude Max 20x price and reset window" -> USD 200/month, 20x Pro per session, rolling 5-hour window.
