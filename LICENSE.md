# NovusTerm — Software License & Terms

**Copyright © 2026 NovusTerm. All rights reserved.**
_Last updated: 13 July 2026._

NovusTerm is **proprietary software**. These terms govern the official build
artifacts (the “Software”) distributed through this repository’s Releases. By
downloading, installing, or using the Software, you agree to these terms. If you do
not agree, do not download, install, or use it.

---

## 1. The licence you get

Subject to these terms, you are granted a **limited, personal, non-exclusive,
non-transferable, revocable** licence to install and run the Software for its
intended purpose — **on the number of devices your tier allows** (section 2).

The Software is **licensed, not sold**. NovusTerm retains all right, title, and
interest in it, including all intellectual property rights. **No licence to any
source code** is granted; this repository contains none.

## 2. Tiers, trial, and how many devices you may use

| Tier | Price | Devices included | Each extra device |
|---|---|---|---|
| **Free** | — | Your own devices | — |
| **Trial** (first launch) | — | 1 | — |
| **Pro Monthly** | $6.99 / month | **1** | $1.99 / month |
| **Pro Quarterly** | $17.99 / quarter | **1** | $4.99 / quarter |
| **Pro Annual** | $49 / year | **2** | $13.99 / year |

- **Free** is a real tier, not a crippled demo. You may use it indefinitely, on your
  own devices. Some features are reserved for Pro, and some collections (workspaces,
  SSH profiles, workflows, panes) have limits.
- **Trial.** On first launch the Software unlocks every Pro feature for **7 days**,
  on that device, at no cost and with no payment method. When it ends the Software
  does not stop working — it reverts to **Free**, and your data stays yours.
- **Pro** unlocks the full feature set on the number of devices in the table above.
  A licence key is **activated per device**. To move a licence to another machine,
  deactivate it on the old one first.
- **Extra devices** may be purchased for any Pro plan at the price shown.

**Do not share your licence key.** It is personal to you. Sharing it, or activating
it on more devices than your tier allows, is a breach of these terms.

## 3. How licence checks work — and what happens offline

You should know exactly what the Software does with your licence, because it does it
without asking:

- After activation, the Software **re-validates your licence roughly once every 24
  hours** against Lemon Squeezy (our licensing provider). This sends your licence key
  and a device identifier. Nothing else.
- **You may work offline for up to 14 days** on an already-activated device. Beyond
  that grace period, Pro features lock until the Software can reach the network
  again. It will never delete your data, and Free features keep working.
- If a licence is refunded, cancelled, or expires, Pro features revert to Free.

## 4. Your data stays on your machine

- The Software has **no telemetry and no analytics**. It does not phone home about
  what you do with it.
- **It never transmits the contents of your terminal** — no scrollback, no commands,
  no output, no file paths. If you send a bug report from inside the app, it carries
  only how the app is *configured* (version, operating system, shell name, language,
  plan), and you read and edit the entire report in your browser before you submit
  it.
- Any AI provider key you configure is stored in your **operating system’s keychain**
  and is never sent to us.
- The only network calls the Software makes on its own are the licence check
  (section 3) and the update check (section 5).

## 5. Updates

The Software checks for updates and can install them. Every update is
**cryptographically signed**, and the Software refuses to install one whose signature
it cannot verify. Updates are provided under these same terms unless they arrive with
their own.

## 6. What you may not do

Except where the law says otherwise, you may **not**:

- copy, redistribute, sell, sublicense, rent, lease, or otherwise make the Software
  available to third parties;
- share, resell, or publish a licence key;
- modify, adapt, translate, or create derivative works of the Software;
- reverse-engineer, decompile, or disassemble the Software, or attempt to derive its
  source code;
- circumvent, disable, or tamper with licensing, activation, or update verification;
- remove, alter, or obscure any proprietary notice, mark, or attribution;
- use the Software to build a competing product, or in any unlawful manner.

## 7. Buying, billing, and refunds

Purchases are handled by **Lemon Squeezy**, acting as our **Merchant of Record**. That
means Lemon Squeezy — not NovusTerm — is the seller of record for your transaction: it
issues your invoice, collects any sales tax or VAT due in your country, and processes
refunds. Their terms govern the sale itself; these terms govern your use of the
Software.

**Refunds:** if the Software does not work for you, ask. Write to
**support@novusterm.com** within **14 days** of purchase and we will refund you, no
interrogation. This is in addition to — never instead of — any refund right the law
already gives you.

## 8. Support

Support is best-effort, from one person.

- **Bugs:** <https://github.com/NovusTerm/novus-term-support/issues>
- **Anything else:** **support@novusterm.com**
- **Security vulnerabilities:** **security@novusterm.com** — never a public issue. See
  [SECURITY.md](https://github.com/NovusTerm/novus-term-support/blob/main/SECURITY.md).

Security reports are acknowledged within **72 hours**. Everything else, within a few
business days.

## 9. No warranty

THE SOFTWARE IS PROVIDED **“AS IS”** AND **“AS AVAILABLE”**, WITHOUT WARRANTY OF ANY
KIND, EXPRESS OR IMPLIED, INCLUDING THE IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE, AND NON-INFRINGEMENT.

NovusTerm runs real shells, real `ssh`, and real programs on your machine, with your
own authority. **You are responsible for the commands you run.**

## 10. Limitation of liability

TO THE MAXIMUM EXTENT PERMITTED BY LAW, NOVUSTERM SHALL NOT BE LIABLE FOR ANY INDIRECT,
INCIDENTAL, SPECIAL, CONSEQUENTIAL, OR PUNITIVE DAMAGES, OR FOR ANY LOSS OF DATA,
PROFITS, OR BUSINESS, ARISING OUT OF OR RELATED TO THE SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES. Our total liability for any claim shall not exceed the
amount you paid for the Software in the twelve months before the claim.

Nothing here limits liability that cannot be limited by law — including for death,
personal injury, fraud, or wilful misconduct.

## 11. Third-party components

The Software includes third-party open-source components, each under its own licence;
those licences continue to govern those components, and nothing here limits your rights
under them.

## 12. Termination

This licence terminates automatically if you breach these terms. On termination you must
stop using the Software and delete all copies. Sections 9, 10, and 13 survive.

## 13. Governing law

These terms are governed by the laws of **Mexico**, without regard to conflict-of-law
rules.

**This does not take away rights you already have.** If you are a consumer, the mandatory
consumer-protection law of the country where you live still applies to you in full,
whatever this section says — including, in the European Union, your statutory right of
withdrawal. And because Lemon Squeezy is the Merchant of Record (section 7), your rights
*as a buyer* are governed by that sale in any case.

## 14. Contact

**support@novusterm.com** · <https://novusterm.com/support>

---

_This is not legal advice. These terms describe what the Software actually does; have
counsel review them before commercial distribution._
