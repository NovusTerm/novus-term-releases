# Changelog

All notable changes to distributed NovusTerm builds are documented here.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

Everything below is built and ready; it ships in the first public release once
feature gating (free vs. paid tiers) is in place.

### Added
- Signed (Apple Developer ID) and **notarized** universal macOS build
  (Apple Silicon + Intel), distributed as a `.dmg` — opens without Gatekeeper
  warnings.
- In-app **auto-update**: the app checks this repo's release feed and installs
  signature-verified updates.
- Terminal workspace: tabs, split & floating panes, saved workspaces and layouts.
- Widgets: file explorer with previews, embedded web browser (with devtools),
  system/process monitor, clock.
- Warp-style command **blocks**, command **palette** (⌘K), and autocompletion.
- SSH remote terminals with saved connections.
- AI assistant panel and per-command "explain/fix" actions.
- Deep theming: ~50 themes, per-pane transparency, fonts, and customization.

### Known issues
- Early beta; expect rough edges. Feedback welcome.

> **Note:** a `v0.1.0` build was briefly published on 2026-07-02 and retracted the
> same day (it predated feature gating). No users were affected.
