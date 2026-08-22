# Project 42 Admin — Agent Instructions

## What this repo is
The owner and administrative console for the official Project 42 hosted platform.

## Start here
Use the HCS Governance MCP server as the standards source of truth:
```text
bootstrap(repo="admin.project-42.dev", client="<client>")
```

## Hard rules
1. Never commit administrative credentials or session keys.
2. Enforce strict authorization and audit event logging.
3. Commit format: `type(scope): description (AB#<id>)`.
