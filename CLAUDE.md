# CLAUDE.md — NovusTerm Releases

> Working context for any AI assistant or contributor in this repository.
> Read this first, every session.

---

## 1. Purpose

This is the **public distribution point** for NovusTerm: it hosts the signed,
notarized macOS build artifacts as GitHub Releases, and serves the auto-update
feed (`latest.json`). It is deliberately public so end users can download the app
and the in-app updater has a reachable feed.

**It is NOT the product.** The application source is proprietary and lives in the
**private** `novus-term-desktop` repo. Nothing here should ever expose that source.

---

## 2. Hard rules

1. **No product source code, ever.** Only distribution artifacts (in Releases, not
   in the git tree) plus repo docs (README, CHANGELOG, this file, `docs/`). If a
   change would add app source, it belongs in `novus-term-desktop`, not here.
2. **No build artifacts in the git tree.** Installers and updater packages
   (`*.dmg`, `*.app.tar.gz`, `*.sig`, `latest.json`, …) live as **release assets**,
   never as files in the repo (they're `.gitignore`d). Small **brand/doc images**
   used by the README (the app icon, logo) are the only permitted binaries, and live
   under `assets/`.
3. **Releases are immutable once published.** Never rewrite or delete a published
   release's assets; ship a new version instead. (Re-generating a bad draft before
   publishing is fine.)
4. **Every release has notes + a CHANGELOG entry.** See §4.
5. **Versioning is SemVer**, tag `vX.Y.Z`, matching the app version built in
   `novus-term-desktop` (`tauri.conf.json` / `package.json` / `Cargo.toml`).
6. **Public means public.** Assume anything added here is world-readable. Never put
   secrets, signing keys, private URLs, or internal notes in this repo.

---

## 3. How a release gets here

Full flow in [`docs/RELEASE-PROCESS.md`](./docs/RELEASE-PROCESS.md). In short: the
private `novus-term-desktop` CI builds + signs + notarizes on a `vX.Y.Z` tag and
publishes the artifacts (`*.dmg`, `*.app.tar.gz`, `*.app.tar.gz.sig`, `latest.json`)
as a Release **in this repo**. The `latest.json` asset URLs must point at **this
repo's** release assets, so the updater endpoint
(`.../novus-term-releases/releases/latest/download/latest.json`) resolves.

---

## 4. Release notes & CHANGELOG (mandatory)

Every published release must carry:

- **Release notes** (the GitHub Release body): what's new — grouped as
  **Added / Changed / Fixed / Security**, plus **Known issues** when relevant, and
  the download line. Write for users, not developers.
- **A `CHANGELOG.md` entry** for that version (Keep a Changelog format, newest on
  top), kept in sync with the release notes. `CHANGELOG.md` is the durable,
  browsable history; the Release body is the same content surfaced at download time.

Keep an `[Unreleased]` section at the top of `CHANGELOG.md` to accumulate changes
between releases; on release, rename it to the version + date.

---

## 5. Conventions

- **English** for all files, commits, docs, and release notes.
- Commits authored solely by the repository owner — **no AI/assistant attribution**
  (no `Co-Authored-By`, no "generated with" notes), matching the product repo's policy.
- Keep it minimal: this repo is infrastructure, not a place for feature work.

---

## 6. Structure

```
novus-term-releases/
├── README.md              user-facing: what this is + how to download
├── CLAUDE.md              this file
├── CHANGELOG.md           running release history (Keep a Changelog)
├── LICENSE.md             proprietary notice (no OSS license)
├── assets/                brand images used by the README (app icon, logo) — the
│                          only binaries allowed in the tree
├── docs/
│   └── RELEASE-PROCESS.md how artifacts are published here + the updater feed
└── .github/
    └── release-notes-template.md  the notes structure to fill per release
```
