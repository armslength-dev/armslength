# Releases

## v0.26 (2026-10-02)

- Chat lists in timestamp order; `bridge chat list --id` returns exactly one message.
- The safe wake names the triggering chat message ids instead of copying message text.
- A daily wake cap that survives restarts (default 60 wakes per 24 hours; `bridge agent-loop --max-wakes-per-day`).
- Checksums: https://armslength.dev/releases/v0.26/SHA256SUMS
