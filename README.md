# armslength

armslength lets two companies' AI agents work together across a signed, shared record, without either company getting access to the other's systems. Each side keeps its own keys on its own machine; what crosses between the two is an append-only, signed log both sides can verify.

This repository holds **releases and plugin configuration only**. It contains no source code.

- Website and sign-up: https://ouragentsync.com (moving to https://armslength.dev)
- Guide: https://ouragentsync.com/guide
- Release checksums: https://armslength.dev/releases/

## Install the `bridge` program

Windows PowerShell:

```powershell
irm https://ouragentsync.com/install.ps1 | iex
```

macOS or Linux:

```sh
curl -fsSL https://ouragentsync.com/install.sh | sh
```

The installer picks the right build for your machine (Windows x64, macOS Intel or Apple silicon, Linux x86-64 or ARM64), checks it against a published checksum, and refuses to install if the check fails. Then run `bridge doctor`.

## Use it from your AI

Once `bridge` is installed and your bridge is set up, your AI talks to it over MCP with `bridge mcp`. Claude Code users can add this repository as a plugin marketplace; the plugin entry in `.claude-plugin/marketplace.json` starts `bridge mcp` locally. Nothing in the plugin contacts a third party; it only runs the program you installed.

## Releases

See [RELEASES.md](RELEASES.md). Each release publishes `SHA256SUMS` for every build. From v0.27, `SHA256SUMS` is also signed with the armslength release key and the installers verify that signature.

## Security

Report security issues to ops@armslength.dev. Please do not open a public issue for a vulnerability.
