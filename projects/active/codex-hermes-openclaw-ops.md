# Codex / Hermes / OpenClaw 环境维护

## Goal

Maintain a lightweight operations memory for the user's local AI tooling across Mac mini, MacBook, Codex Desktop, Hermes, OpenClaw, local model gateways, and network proxy routes.

## Scope

This project tracks:

- Codex Desktop connectivity and GitHub memory repo setup
- Local Codex proxy bridge
- Hermes dashboard and gateway
- Claude-MiMo / Xiaomi MiMo local gateway
- OpenClaw gateway and model configuration
- Router / node / proxy symptoms that affect model calls
- Cross-device memory workflow between Mac mini and MacBook

## Known Local Services

- Codex memory repo:
  - Local: `/Users/qiufeng/Library/Mobile Documents/com~apple~CloudDocs/codex-memory`
  - GitHub: `https://github.com/qf34shangxue-droid/codex-memory.git`
- Codex proxy bridge:
  - Common local endpoint: `127.0.0.1:18790`
- OpenClaw:
  - Common dashboard endpoint: `127.0.0.1:18789`
- Hermes:
  - Common dashboard endpoint: `127.0.0.1:9119`
- Local MiMo / model gateway:
  - Common endpoint: `127.0.0.1:4000`

## Recent Stable Findings

- `codex-memory` was initialized, committed, and pushed to GitHub on 2026-06-17.
- MacBook cloned the private repository to `/Users/hitman/Documents/codex-memory` on 2026-06-22 and configured global Codex startup rules for safe pull, update, commit, push, and conflict handling.
- GitHub CLI is authenticated for `qf34shangxue-droid` via system keyring.
- Git operations are configured to use GitHub CLI credential helper.
- Do not print or store GitHub tokens.

## Common Symptoms And First Checks

### `stream disconnected before completion: tls handshake eof`

Likely area:

- Network node / proxy route instability
- ChatGPT backend or WebSocket path interruption

First checks:

- Confirm local proxy bridge is running.
- Check whether `codex doctor` reports WebSocket `HTTP 101 Switching Protocols`.
- Try a stable US node if failures repeat.

### Hermes slow task execution

Likely area:

- Large context model calls
- Local model gateway latency
- Model provider error / fallback

First checks:

- Confirm `127.0.0.1:9119` is serving dashboard.
- Confirm `127.0.0.1:4000` returns local gateway health.
- Check recent Hermes errors for 401 / 500 / timeout.

### OpenClaw model failures

Likely area:

- Provider/model registration mismatch
- Expired or stale gateway process state
- Node/proxy instability

First checks:

- Confirm dashboard/gateway at `127.0.0.1:18789`.
- Confirm model provider registration matches the working provider path.
- Restart gateway only after identifying the failed component.

## Safety Rules

Never store in this memory repo:

- API keys
- OAuth tokens
- GitHub tokens
- router credentials
- browser cookies
- `.env` values
- Codex `auth.json`
- Codex session databases
- Hermes/OpenClaw raw secrets
- SQLite state/log databases

This file should contain only operational memory, endpoints, symptoms, and safe procedures.

## Next Likely Tasks

- Optionally create a small health-check checklist for Codex/Hermes/OpenClaw.

## History

- 2026-06-17: Added first active project memory entry.
- 2026-06-22: Connected MacBook at `/Users/hitman/Documents/codex-memory` and added global Codex memory workflow rules.
