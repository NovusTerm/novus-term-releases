# Third-Party Notices — NovusTerm

NovusTerm is built on open-source software. This file lists the third-party
components distributed in the Software and the licenses under which they are
provided. Each component remains the property of its respective authors and is
licensed to you under its own terms, which govern that component. These components
are provided **"as is," without warranty of any kind.**

> **How this list is maintained.** The entries below are the direct, bundled
> dependencies. A full, transitive list (every crate and npm package, with its exact
> license text) should be generated at release time with `cargo about generate`
> (Rust) and a JavaScript license aggregator (e.g. `license-checker` /
> `oss-attribution-generator`) and shipped in-app under **About → Open-Source
> Licenses**. This document is the human-readable summary; the generated report is
> the authoritative, complete record.

---

## Frontend (JavaScript / TypeScript)

| Component | License |
|---|---|
| React (`react`, `react-dom`) | MIT |
| xterm.js (`@xterm/xterm`, `@xterm/addon-fit`, `@xterm/addon-search`, `@xterm/addon-web-links`) | MIT |
| `@tauri-apps/api` and Tauri plugins (clipboard-manager, dialog, process, store, updater) | MIT / Apache-2.0 |
| DOMPurify (`dompurify`) | MPL-2.0 OR Apache-2.0 |
| highlight.js (`highlight.js`) | BSD-3-Clause |
| JSZip (`jszip`) | MIT OR GPL-3.0-or-later (used under **MIT**) |
| Mammoth (`mammoth`) | BSD-2-Clause |
| PDF.js (`pdfjs-dist`) | Apache-2.0 |
| react-markdown, remark-gfm, rehype-highlight | MIT |
| SheetJS (`xlsx`, community build) | Apache-2.0 |

### Bundled fonts (`@fontsource/*`)

Cascadia Code, DM Mono, Fira Code, Geist Mono, IBM Plex Mono, Inconsolata,
JetBrains Mono, Martian Mono, Roboto Mono, Source Code Pro, Space Mono, Ubuntu Mono,
and Victor Mono. Each is distributed under the **SIL Open Font License 1.1** and/or
**Apache License 2.0**, as stated in that font's package. The OFL permits bundling
the fonts within the application; it does not permit selling the fonts by themselves,
and reserved font names are used only as permitted.

---

## Backend (Rust crates)

| Crate | License |
|---|---|
| Tauri (`tauri`, plugins) | MIT / Apache-2.0 |
| `portable-pty` (part of wezterm) | MIT |
| `serde`, `serde_json` | MIT / Apache-2.0 |
| `sysinfo` | MIT |
| `battery` | MIT / Apache-2.0 |
| `reqwest` | MIT / Apache-2.0 |
| `keyring` | MIT / Apache-2.0 |
| `zeroize` | MIT / Apache-2.0 |
| `tokio`, `futures-util` | MIT |
| `trash` | MIT / Apache-2.0 |
| `notify` | CC0-1.0 / Artistic-2.0 |
| `hmac`, `sha2` | MIT / Apache-2.0 |
| `objc2`, `block2` | MIT |
| `libc` | MIT / Apache-2.0 |

Plus the transitive dependencies of the above, each under its own MIT / Apache-2.0 /
BSD / similar permissive license. The complete transitive list with full license
texts is generated at release time (see the note at the top of this file).

---

## License texts

The full text of the MIT, Apache-2.0, BSD-2-Clause, BSD-3-Clause, MPL-2.0, and SIL
OFL 1.1 licenses accompanies the components that use them and is reproduced in the
generated in-app **Open-Source Licenses** report. Copies are also available from each
project's repository and from the respective license steward (e.g.
https://opensource.org/licenses and https://openfontlicense.org).

---

_If you believe a component is missing from this list or is misattributed, please
contact us (see the EULA, §14) and we will correct it._
