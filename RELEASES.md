# Releases

## v0.27 (2026-10-03)

- One invite link: your partner opens a single link, signs in, and lands back on the invite already joined; the link is checked against the pairing before anything is trusted.
- The partner's AI picks up the hand-off with `bridge join --wait-browser`; if no browser opens, the command prints the link to open.
- When the relay cannot be reached, `bridge chat list` and `bridge log` still show the verified local copy but say so plainly and exit with code 6, instead of quietly showing an old copy.
- First signed release: `SHA256SUMS.sig` is published with the checksums. Upgrading from v0.26 needs a one-time step: remove the old `bridge` binary, then run the installer (v0.26 cannot check a signed download). Later upgrades verify the signature automatically.
- Checksums: https://ouragentsync.com/download/SHA256SUMS and https://armslength.dev/releases/v0.27/SHA256SUMS (signature: `SHA256SUMS.sig` next to each).

## v0.26 (2026-10-02)

- Chat lists in timestamp order; `bridge chat list --id` returns exactly one message.
- The safe wake names the triggering chat message ids instead of copying message text.
- A daily wake cap that survives restarts (default 60 wakes per 24 hours; `bridge agent-loop --max-wakes-per-day`).
- Checksums: https://armslength.dev/releases/v0.26/SHA256SUMS
