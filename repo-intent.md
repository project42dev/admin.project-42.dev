# Repo intent — admin.project-42.dev

**Project 42 owner administration console — deployed build output, not source.**

## What this repo is

The repo root holds compiled Next.js output (`_next/`, `pages-manifest.json`,
`vinext-client-entry-manifest.json`, `release-facts.json`) rather than application
source — this is a **deploy target repo**, most likely built and pushed here by CI
from a source repo elsewhere in the org. No README exists to confirm the exact
source repo as of this writing.

## What this repo is not

- Not where the admin console's source code lives — treat this as generated output;
  don't hand-edit files here expecting changes to persist past the next deploy

## Status

Active (serving), but **undocumented**. Whoever next touches this repo's deploy
pipeline should update this file with the actual source repo and deploy mechanism.
