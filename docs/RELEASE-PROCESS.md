# Release process

How a NovusTerm build gets from source to a public download here.

## Overview

```
novus-term-desktop (PRIVATE)                 novus-term-releases (PUBLIC, this repo)
  push tag vX.Y.Z                                     Release vX.Y.Z
  └─ CI: build universal ─ sign (Developer ID)        ├─ NovusTerm_X.Y.Z_universal.dmg
        ─ notarize (Apple) ─ staple                   ├─ NovusTerm_universal.app.tar.gz (+ .sig)
        └─ publish artifacts here ───────────────────►├─ latest.json   ← updater feed
                                                       └─ release notes (+ CHANGELOG entry)
```

The **source stays private**; only the finished, signed artifacts are published
here, where they're world-downloadable and the auto-updater can reach `latest.json`.

## Steps

1. In `novus-term-desktop`, bump the version (`tauri.conf.json`, `package.json`,
   `src-tauri/Cargo.toml`) and update its `CHANGELOG`.
2. Tag `vX.Y.Z` and push — the release workflow builds, signs (Apple Developer ID),
   and notarizes a universal macOS build.
3. The CI publishes the artifacts as a **draft** Release **in this repo** (`vX.Y.Z`):
   `*.dmg`, `*.app.tar.gz`, `*.app.tar.gz.sig`, `latest.json` (cross-repo publish —
   see below).
4. Add this repo's `CHANGELOG.md` entry for `vX.Y.Z` (mirror the release notes) and
   fill the release body from [`.github/release-notes-template.md`](../.github/release-notes-template.md).
5. Publish the release. `.../releases/latest` now points at it, so the download link
   and the updater feed are live.

## The updater feed

- The app polls `https://github.com/NovusTerm/novus-term-releases/releases/latest/download/latest.json`.
- GitHub's `/releases/latest/...` resolves to the newest **non-prerelease** release,
  so **publish stable updates as normal releases** (not "pre-release") for the
  updater to serve them. Beta/pre-release builds are still downloadable from their
  own release page, but won't be offered as an auto-update.
- `latest.json`'s asset URLs must point at **this** repo's assets (not the private
  repo), or the updater download 404s.

## Cross-repo publishing (automated)

The private repo's CI publishes **directly into this public repo** using
tauri-action's cross-repo `owner`/`repo` inputs, authenticated with a
`RELEASES_REPO_TOKEN` secret — a fine-grained PAT scoped to `contents: write` on
`novus-term-releases` only (the default `GITHUB_TOKEN` can't write across repos).
tauri-action writes `latest.json` with **this repo's** asset URLs automatically, so
there is no manual URL rewrite. The release lands here as a **draft**; a human
finalizes the notes + CHANGELOG entry and publishes.

If the PAT is ever removed, the workflow falls back to drafting in the private repo,
and releases can be copied here manually with `gh release create`.
