# Guardrails Governance (`grg`)

A focused BMad module for privacy, legal and licensing, regulatory compliance, and live legal updates. It separates actual obligations from common practice and identifies rules that do not apply.

This is a focused BMad module in the [Guardrails](https://github.com/mlarese/bmad-module-guardrails)
bundle. It keeps the same behavior and shared memory while installing only the figures and
workflows for the governance area.

> **Generated.** This repository is produced by `tools/build_modules.py` in the
> [bmad-module-guardrails](https://github.com/mlarese/bmad-module-guardrails) repository.
> Make changes there and regenerate; local changes here will be overwritten.

## Agents

| Agent | Role | Skill | Focus |
| ----- | ---- | ----- | ----- |
| 🛡️ Vera | Data Protection Officer | `grl-agent-privacy` | Personal data, GDPR, DPIAs, retention, analytics, logs, and data in prompts. |
| ⚖️ Aldo | Tech Lawyer | `grl-agent-legal` | Licenses, contracts, DPAs, ownership, AI outputs, and AI Act obligations. |
| 📐 Nils | Regulatory Compliance | `grl-agent-compliance` | NIS2, DORA, EAA/WCAG, eIDAS, CRA, MDR, and sector-specific obligations. |

## Skills and workflows

| Skill | Purpose |
| ----- | ------- |
| `grg-profile` | Project profile | Collects the project context shared by every installed figure. |
| `grg-board` | Multidisciplinary review | Convenes the relevant figures on one artifact and returns a review summary or release verdict. |
| `grl-legal-updates` | Live legal updates | Searches primary sources for laws, decrees, rulings, and amendments in a defined period, with coverage and freshness checks. |
| `grl-automation` | Controlled automation | Routes work from read-only checks through dry-run to observable execution, with explicit approvals and rollback. |

## Installation

```
bmad install grg
```

As a first step, run `grg-profile`. It collects the project profile — sector, data,
market, stack, and criticality — so each figure can calibrate its review. Without a profile,
the default remains `normal` and the figures start without context.

## Shared memory

The profile lives in `{project-root}/_bmad/memory/grl-shared/project-profile.md`, together
with `decisions.md` and `accepted-risks.md`. All Guardrails modules use the same path, so two
installed modules still share one profile.

## Using it with the bundle

This module installs skills with **the same names** as the `grl` bundle — `grl-agent-privacy`
is identical in both. Do not install the full bundle and thematic modules in the same project:
choose the complete bundle, or only the thematic modules you need.

## License

MIT.
