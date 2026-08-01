# admin.project-42.dev

Project 42's owner administration console, per
[ADR-0009's 2026-08-01 amendment](https://github.com/project42dev/project42dev-ops/blob/main/pmo/adrs/0009-owner-administration-surface.md).

This repository is currently a placeholder: it establishes the GitHub Pages
deployment and DNS boundary ahead of migrating the owner console out of
`learn.project-42.dev/admin`. Until that migration lands, the console remains
at `learn.project-42.dev/admin`.

## Hosting

- GitHub Pages, deployed via `.github/workflows/deploy-pages.yml` on every push
  to `main`.
- DNS-only CNAME to `project42dev.github.io` (Cloudflare), matching the
  `learn.`/`guide.` pattern from `SPIKE-008-three-site-cutover.md`.
- No application code yet — see `project42dev-ops` for the migration plan.

## Security

Authorization for every privileged operation stays entirely server-side in the
Cloudflare Worker API (`project42-platform`). This origin, once it hosts the
real console, is presentation defense-in-depth only — never the security
boundary.
