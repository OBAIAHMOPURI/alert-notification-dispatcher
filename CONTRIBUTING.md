# Contributing to Alert Notification Dispatcher

[Root README](README.md) · [Architecture](docs/ARCHITECTURE.md) · [Setup](docs/SETUP.md) · [API guide](docs/API.md) · [Network Ecosystem](README.md#network-ecosystem)

## Project status

This repository is a documentation-first scaffold. There is no notification implementation, provider integration, configured recipient list, executable, or automated test suite. Design notes are proposals, not permission to send messages or promises of working delivery.

## Start with a small, reviewable change

Read the linked guides and agree the problem and acceptance criteria with the owner. For a local documentation change:

```sh
git clone https://github.com/OBAIAHMOPURI/alert-notification-dispatcher.git
cd alert-notification-dispatcher
git switch -c docs/describe-change
```

Use a focused branch and pull request for normal contributions. Direct-to-main publication for this documentation batch was specifically owner-authorized; it does not establish a standing merge policy. Do not add guessed install commands or dependencies before a runtime is selected.

## Repository-specific priorities

- Agree alert schemas, approved channels, recipient-policy ownership, consent/opt-out behavior, quiet hours, timezones, and escalation limits.
- Define a stable deduplication key, durable outbox/attempt ledger, bounded retries, and a safe sandbox-only adapter.
- Distinguish provider acceptance, delivery, and human acknowledgement; do not label all three as delivered.
- Keep gateway, identity, telemetry, and workflow relationships explicitly proposed until contracts and tests exist.

## Evidence and review checklist

- State whether the change is documentation, a proposal, or implemented functionality.
- For code, add reproducible prerequisites and tests with synthetic fixtures; cover duplicates, template escaping, invalid recipients, rate limits, provider errors, and replay without duplicate sends.
- Run `git diff --check`; review Markdown rendering, relative links, the root README backlink, and all seven sibling links.
- Report exact commands actually run and their outcomes. Say when tests were not run; no existing CI or passing test result is implied.
- Include scope, rationale, test evidence, limitations, compatibility effects, and any migration/rollback needs in the pull request. Update setup/API/architecture notes with behavior changes.

## Security and operational safety

Never commit provider credentials, tokens, real recipient lists, private operational notes, or raw personal data. Use synthetic payloads and approved sandbox destinations. Sending messages, enabling live integrations, provisioning infrastructure, or changing access requires separate authorization. Report sensitive vulnerabilities privately through an owner-approved channel rather than disclosing secrets in a public issue. No license file is currently established; this guide does not select a license.

## Sibling repository network

These links are documentation navigation, not implemented runtime integrations.

- [Brainwave_Matrix_Intern — Banky Application](https://github.com/OBAIAHMOPURI/Brainwave_Matrix_Intern/blob/main/README.md)
- [BrainWave_Matrix_Intern1 — Hospital Management System](https://github.com/OBAIAHMOPURI/BrainWave_Matrix_Intern1/blob/main/README.md)
- [edge-gateway-service](https://github.com/OBAIAHMOPURI/edge-gateway-service/blob/main/README.md)
- [edge-gateway-service1](https://github.com/OBAIAHMOPURI/edge-gateway-service1/blob/main/README.md)
- [identity-auth-proxy](https://github.com/OBAIAHMOPURI/identity-auth-proxy/blob/main/README.md)
- [telemetry-stream-worker](https://github.com/OBAIAHMOPURI/telemetry-stream-worker/blob/main/README.md)
- [workflow-state-sync](https://github.com/OBAIAHMOPURI/workflow-state-sync/blob/main/README.md)
