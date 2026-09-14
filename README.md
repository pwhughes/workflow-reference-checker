# Optomatic Workflow Reference Checker

A browser-local check for repository maintainers who want to spot mutable external GitHub Actions references before a workflow runs.

## What it checks

Paste a workflow YAML file. The free check identifies external `uses:` references that are not pinned to a full commit SHA. It does not access repositories, change workflows, upload source code, or make a security certification.

## Use the live checker

Open **https://workflow-reference-checker.optomatic.app**. Your YAML stays in your browser.

## Paid deliverable — €9 one time

After a successful Stripe Checkout payment, the same browser can download a timestamped workflow-reference report containing the diagnostic findings and submitted text. There is no subscription and no account requirement.

## Example

```yaml
name: CI
uses: actions/checkout@v4
```

The free check will flag the mutable tag. A full 40-character commit SHA is the narrow immutable-reference boundary this checker recognizes.

## Limits

This is a deterministic workflow-text review aid, not a complete security audit or compliance advice. Review all workflow changes in your normal engineering process.

Built by [Optomatic](https://optomatic.app). Privacy and contact details are on the live product page.
