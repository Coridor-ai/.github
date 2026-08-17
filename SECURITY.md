<!-- coridor-sdlc managed file - synced from Coridor-ai/coridor-sdlc; edit there, not here. template-version: b984efe6da4e317b56398f71241c21afa2d9f5d87147b390a8504fa6f7aa1d98 -->

# Security Policy

## Reporting a vulnerability

Email **hub@coridor.ai**. Include what you found, where, reproduction steps, and impact as you understand it.

Do NOT open a public issue for a vulnerability. Do not put exploit details in PR descriptions, commit messages, or comments. Public disclosure before a fix ships puts every user at risk.

## What happens next

- Acknowledgment within 2 business days.
- Severity assessment within 5 business days of acknowledgment.
- Remediation runs on severity-based SLAs, aligned to CVSS v3.1 bands:

| Severity | CVSS | Remediation SLA |
|---|---|---|
| Critical | 9.0-10.0 | 7 days |
| High | 7.0-8.9 | 30 days |
| Medium | 4.0-6.9 | 90 days |
| Low | 0.1-3.9 | 180 days |

The internal [vulnerability management policy](https://github.com/Coridor-ai/coridor-sdlc/blob/main/docs/policies/vulnerability-management-policy.md) is canonical; if this table and the policy disagree, the policy wins. (The link requires Coridor-ai org access -- the table above is the commitment to external reporters.)

We'll keep you informed through triage and fix, and credit you on disclosure unless you'd rather we didn't.

## Supported versions

We support branches, not version numbers. The branch model is `dev -> uat -> main` (see coridor-sdlc, ADR-0010).

| Branch | Meaning | Security fixes |
|--------|---------|----------------|
| `main` | production | [ok] always - hotfixes land here first when critical |
| `uat`  | acceptance candidate | [ok] via promotion from `dev` or hotfix back-merge |
| `dev`  | integration | [~] fixed in the normal flow; not independently patched |
| anything else (old tags, archived repos) | - | [-] not supported |

Last updated: 2026-07-02
