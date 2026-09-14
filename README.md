# ActionPin


ActionPin is a browser-only diagnostic for one common CI supply-chain footgun: mutable GitHub Actions references such as `actions/checkout@v4`. A tag can move; a full commit SHA cannot.

## Free diagnostic

Paste a workflow YAML file at https://optomatic-holdco.vercel.app/lab/live-cohort/actionpin . The check runs locally in your browser—no repository access, token, workflow file, or source code is uploaded.

It flags action references that are not pinned to a full commit SHA so you can decide what to change before CI runs.

## Paid deliverable — €9 one time

For a workflow you have checked, ActionPin offers a CI action-pinning report: a structured record of mutable action references and the recommended pinning boundary. Checkout is one-time, with no subscription.

Buy from the diagnostic page only if the free result identifies an issue you need to document.

## Limits

ActionPin is a lightweight diagnostic, not a security audit or a replacement for code review. It does not modify workflows, access repositories, or make compliance claims.

## Why this exists

Workflow dependencies are executable supply-chain inputs. Pinning third-party actions to immutable commit SHAs narrows the risk from a moved or compromised tag.
