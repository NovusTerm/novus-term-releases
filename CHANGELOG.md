# Changelog

All notable changes to distributed NovusTerm builds are documented here.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

Everything below is built and ready for the first public release. Free vs. Pro
gating is in place (enforced in the Rust core), with a 7-day fully-unlocked trial
on first launch. Items marked **(Pro)** require a subscription.

### Added
- Signed (Apple Developer ID) and **notarized** universal macOS build
  (Apple Silicon + Intel), distributed as a `.dmg` — opens without Gatekeeper
  warnings.
- In-app **auto-update**: the app checks this repo's release feed and installs
  signature-verified updates.
- Terminal workspace: tabs, split panes, saved workspaces and layouts.
  Floating panes and synchronized input **(Pro)**.
- Widgets: file explorer with image/PDF/code/markdown/CSV previews, embedded web
  browser (with devtools), system/process monitor, clock.
  Video, audio and Office previews, folder search and bookmarks **(Pro)**.
  Process termination, per-process details and disk/network I/O **(Pro)**.
- Warp-style command **blocks**, command **palette** (⌘K), and autocompletion.
  Searching past command output — the time machine — **(Pro)**.
- SSH remote terminals with saved connections and your own keys.
  Jump / bastion hosts **(Pro)**.
- AI assistant chat pane with your own API key.
  Per-command "explain / fix" actions and the agent console **(Pro)**.
- Deep theming: **55 themes** (40 dark, 15 light), 13 fonts, per-pane transparency —
  all free. Automatic theme rotation **(Pro)**.
- Licensing: 7-day trial, then Free forever or Pro from **$6.99/month**
  (**$49/year**, covering 2 Macs). No account required — the license key is the
  access. Billing opens soon.

### Known issues
- Early beta; expect rough edges. Feedback welcome.

> **Note:** a `v0.1.0` build was briefly published on 2026-07-02 and retracted the
> same day (it predated feature gating). No users were affected.
