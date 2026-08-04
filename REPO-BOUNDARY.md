# Repository boundary

This file states what this repository is for, what must never be added to it,
and where to look instead. It exists because two codebases ended up in the
wrong repositories, and both got there through a directory convention that
nobody enforced.

Governing decision: **ADR-0017**, Orchard and the Foundry layer separation.

## What this is

**The owner administration console: operational control of the hosted instance.**

- Visibility: **public**

## What must never go here

| Do not add | Because | Where it belongs |
|---|---|---|
| **Anything learner facing** | A console is not a product surface. | `learn.`, `guide.`, `account.` |
| **Real learner data or exports of it** | Public repository. | The runtime data store |
| **Secrets, connection strings, or credentials of any kind** | Public repository, and this is the repository most likely to be handed one. | The operator's own secret store |
| **Content authoring** | Administration operates the platform; it does not write for it. | `orchard` |

## Looking for something else?

| Looking for | It lives in |
|---|---|
| The content, the content model, and the schemas | `project42-platform` |
| The content lifecycle tool: discovery, authoring, currency | `orchard` |
| The public marketing and entry surface | `project-42.dev` |
| The Learn delivery surface | `learn.project-42.dev` |
| The Field Guide delivery surface | `guide.project-42.dev` |
| Learner account and profile | `account.project-42.dev` |
| Planning, sprints, ADRs, board records | `project42dev-ops`, private |
| An Azure AI Foundry deployment framework | `homestead-foundry` |
| One owner's Foundry instance and model registry | `my-homestead-foundry` |

## The rule in one line

**This repository operates the platform. It never becomes part of the product.**
