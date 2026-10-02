# Releases

## v0.26 (2026-10-02)

- Chat lists in timestamp order; `bridge chat list --id` returns exactly one message.
- The safe wake names the triggering chat message ids instead of copying message text.
- A daily wake cap that survives restarts (default 60 wakes per 24 hours; `bridge agent-loop --max-wakes-per-day`).
- Checksums: https://armslength.dev/releases/v0.26/SHA256SUMS

## Coming in v0.27

- One-link partner onboarding: the partner opens one link, signs in, and connects their computer from the page with a typed connect code. No secrets pasted into a chat.
- Signed releases: `SHA256SUMS.sig` verified by the installers against the pinned armslength release key.
